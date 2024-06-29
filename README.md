# proxychains.conf

proxychains é uma ferramenta de redes usada no mundo da T.I para preservar a  identidade anônima na internet,ele é um programa que permite o encaminhamento de conexões de rede através deuma cadeia de proxies,fornecendo a segurança adicional e o anonimato,muito usada por grupos de hackers ativistas para preservar sua identidade e zelar por seu movimento e questão cultural e ideológica.

O Proxychains permite que o tráfego de rede seja encaminhado através de uma série de proxies. Isso pode incluir proxies HTTP, SOCKS4, e SOCKS5 onde o socks5 é mais seguro que seu antecessor
A principal vantagem é que cada requisição de rede passa por múltiplos servidores proxy antes de alcançar o destino final, mascarando a origem do tráfego.

SOCKS5: Permite autenticação, o que significa que você pode configurar o proxy para exigir um nome de usuário e senha. Isso adiciona uma camada de segurança, garantindo que apenas usuários autorizados possam usar o proxy,inclusive muitos desses proxies podem vir de fontes de roteamento onion da rede tor que contam com milhares de proxies administrados por milhares de usuarios do mundo,ao qual torna impossivel identificar quem é você na rede,mas lógico nenhum software está seguro aos erros humanos

SOCKS5: Pode encaminhar qualquer tipo de tráfego de rede, incluindo UDP (User Datagram Protocol), o que o torna útil para uma ampla gama de aplicações, como DNS (Domain Name System) e serviços de streaming. Isso oferece mais flexibilidade e suporte para aplicativos modernos que dependem de diferentes tipos de tráfego.
SOCKS4: Suporta apenas TCP (Transmission Control Protocol), limitando seu uso a tipos específicos de tráfego.

SOCKS5: Pode ser combinado com outras tecnologias de criptografia, como SSH (Secure Shell) ou TLS (Transport Layer Security), para criar túneis seguros, aumentando a confidencialidade e a integridade dos dados.
SOCKS4: Embora também possa ser encapsulado em túneis SSH, não oferece suporte nativo para esses recursos avançados além de poderem usar uma chave de autenticação chamada pgp (pretty good privacy) que apenas quem criou pode quebrar o que acrescenta ua camada a mais de segurança,além de que esses proxies são usados em altas quantidades por hackers que querem preservar suas identidades,os proxies vem de todo o mundo.


`instalação dos proxyschains`

`Debian/Ubuntu` bash`

`sudo apt update`
`sudo apt install proxychains`

`Arch Linux bash`

`sudo` `pacman` -S `proxychains`

`Fedora` `bash`

`sudo` `dnf` `install` `proxychains`



configuração dos proxyschains pelo nano e arquivo de texto

# proxychains.conf
#
# Tipo de proxies
#
# Dynamic - Se um proxy falhar, tenta o próximo
# Strict - Usa a cadeia na ordem especificada, não ignorando nenhum proxy
# Random - Usa proxies de forma aleatória

dynamic_chain
#strict_chain
#random_chain

# Formato do proxy:
# tipo  IP       porta [username] [password]
# Exemplos:
# socks4  127.0.0.1 9050
# socks5  127.0.0.1 1080
# http    192.168.1.1 8080

[ProxyList]
socks5  127.0.0.1 9050
