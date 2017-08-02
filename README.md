
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "") package ${PACKAGE_NAME};#end
import org.junit.Test;
import com.kyushu.autosum.configuration.AbstractIntegrationTest;
import org.springframework.beans.factory.annotation.Autowired;
import static org.junit.Assert.*;
## Set variable 
#set( $variable = $NAME.substring(0,1).toLowerCase() + $NAME.substring(1))
#parse("Integration Test Header.java")
public class ${NAME}_IT extends AbstractIntegrationTest{

    private ${NAME} ${variable};

    @Autowired
    public void set${NAME}(${NAME} ${variable}) {
        this.${variable} = ${variable};
    }

}
