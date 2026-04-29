import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestHeader;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;
import jakarta.servlet.http.HttpServletRequest;

@RestController
public class MinhaControladoraWeb {

    // ========================================================================
    // 1. Aplicação que escreve "Olá mundo" na tela (Mapeado na raiz da URL)
    // ========================================================================
    @GetMapping("/")
    public String olaMundo() {
        return "Olá mundo";
    }

    // ========================================================================
    // 2.a. Endereço /requisicao exibindo Método, URI e Protocolo
    // ========================================================================
    @GetMapping("/requisicao")
    public String exibirRequisicao(HttpServletRequest request) {
        // Utilizando a tag HTML <br> para quebrar a linha na tela do navegador
        return "Método: " + request.getMethod() + "<br>" +
               "URI do Pedido: " + request.getRequestURI() + "<br>" +
               "Protocolo: " + request.getProtocol();
    }

    // ========================================================================
    // 2.b. Endereço /cabecalhos exibindo host, user-agent, accept-encoding e accept-language
    // ========================================================================
    @GetMapping("/cabecalhos")
    public String exibirCabecalhos(
            @RequestHeader(value = "host", defaultValue = "Não informado") String host,
            @RequestHeader(value = "user-agent", defaultValue = "Não informado") String userAgent,
            @RequestHeader(value = "accept-encoding", defaultValue = "Não informado") String acceptEncoding,
            @RequestHeader(value = "accept-language", defaultValue = "Não informado") String acceptLanguage) {
        
        return "Host: " + host + "<br>" +
               "User-Agent: " + userAgent + "<br>" +
               "Accept-Encoding: " + acceptEncoding + "<br>" +
               "Accept-Language: " + acceptLanguage;
    }

    // ========================================================================
    // 2.c. Endereço /saudacao recebendo o parâmetro 'nome' pela URL
    // ========================================================================
    @GetMapping("/saudacao")
    public String exibirSaudacao(@RequestParam("nome") String nome) {
        return "Olá, " + nome + "!";
    }
}
