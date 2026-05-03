# 🐦 Ferramenta de Análise de Vídeos do X.com

> Uma ferramenta leve, rápida e multifuncional para extrair conteúdo de vídeo do X (anteriormente Twitter)

[🌐 Demonstração online](https://twittervideodownloaderx.com/po) • [📝 Guia de uso](#-guia-de-uso) • [❓ Perguntas frequentes](#-perguntas-frequentes)

---

## 📋 Visão geral do projeto

Este projeto é uma ferramenta de análise de vídeo baseada na web, projetada para extrair com segurança recursos de vídeo de publicações públicas no X.com (anteriormente Twitter), oferecendo opções de conversão e download em múltiplos formatos. Não requer instalação de software cliente nem registro de conta: utilize diretamente pelo seu navegador.

> ⚠️ **Aviso importante**: Esta ferramenta destina-se exclusivamente a fins de aprendizado pessoal, pesquisa técnica e uso dentro de limites razoáveis. Por favor, respeite o [Acordo de Desenvolvedor da Plataforma X](https://developer.twitter.com/en/developer-terms/agreement) e as leis de direitos autorais aplicáveis em seu país. É estritamente proibido o uso para fins que violem direitos de terceiros.

---

## ✨ Funcionalidades principais

- 🔗 **Análise de links**: Compatível com URLs padrão de publicações do X.com; detecção automática de vídeos e GIFs animados
- 📥 **Exportação em múltiplos formatos**:
  - Vídeo MP4 com qualidade original
  - Extração de áudio → Formato MP3
  - Clipe de vídeo → Conversão para GIF animado
- 🌍 **Interface multilíngue**: Suporte para português, inglês, chinês, japonês, coreano e até 16 idiomas no total
- 📱 **Compatibilidade multiplataforma**: Funciona perfeitamente em Chrome / Firefox / Safari / Edge; experiência otimizada para dispositivos móveis e tablets
- 🔒 **Privacidade em primeiro lugar**: Nenhum registro de conta necessário, nenhuma coleta de dados pessoais; processo de análise totalmente anônimo
- ⚡ **Processamento rápido**: Análise concluída em média em menos de 5 segundos; suporte para solicitações simultâneas

---

## 🚀 Início rápido

### Uso online (recomendado)
1. Acesse [https://twittervideodownloaderx.com/po](https://twittervideodownloaderx.com/po)
2. Copie o link da publicação de destino (exemplo: `https://x.com/user/status/123456789`)
3. Cole o link no campo de entrada → Clique no botão 「Analisar」
4. Selecione o formato desejado → Salve o arquivo seguindo as instruções do navegador

### Implantação local (para desenvolvedores)
```bash
# Clonar o repositório
git clone https://github.com/your-repo/x-video-parser.git

# Instalar dependências
cd x-video-parser && npm install

# Configurar variáveis de ambiente (opcional)
cp .env.example .env

# Iniciar servidor de desenvolvimento
npm run dev
```

> 💡 Nota: Este projeto utiliza uma arquitetura baseada em Node.js + Express. Consulte a documentação detalhada de implantação em `/docs/DEPLOY.md`

---

## 🛠 Stack tecnológico

| Módulo | Tecnologias utilizadas |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Processamento de vídeo | ffmpeg.wasm (conversão leve no frontend) |
| Proxy de encaminhamento | Cloudflare Workers / Middleware personalizado |
| Internacionalização | vue-i18n + Pacotes de idioma JSON |

---

## 📚 Guia de uso

### Fluxo operacional básico
```
1. Obter o link da publicação
   └─ Abra a publicação de destino no X.com → Copie a URL da barra de endereços do navegador

2. Enviar solicitação de análise
   └─ Cole o link no campo de entrada da ferramenta → Clique em 「Baixar vídeo」

3. Selecionar formato de saída
   ├─ 🎬 Baixar como MP4: Salvar com qualidade original
   ├─ 🎵 Converter para MP3: Extrair faixa de áudio
   └─ 🎞 Converter para GIF: Gerar animação curta (recomendado: ≤15 segundos)

4. Salvar o arquivo
   └─ O recurso será aberto em uma nova aba → Clique direito/menu → 「Salvar como」
```

### Dicas para uso em dispositivos móveis
- iOS Safari: Botão Compartilhar → 「Salvar em Arquivos」
- Android Chrome: Pressionar e segurar o vídeo → 「Baixar vídeo」
- Se o vídeo reproduzir automaticamente: Clique em `⋮` no canto superior direito do player → Selecione 「Baixar」

---

## ❓ Perguntas frequentes

**P: Onde os arquivos baixados são salvos?**  
R: Os arquivos são salvos na pasta de download configurada no seu navegador. Você pode verificar ou alterar este caminho nas configurações do navegador.

**P: Posso analisar contas privadas ou conteúdo restrito?**  
R: Não. Esta ferramenta funciona apenas com publicações configuradas como públicas e respeita as configurações de acesso do conteúdo original.

**P: A qualidade de imagem/áudio é reduzida após a conversão?**  
R: O formato MP4 mantém a qualidade original. O formato MP3 utiliza codificação padrão de 128 kbps. O formato GIF otimiza a taxa de quadros conforme a duração para equilibrar tamanho do arquivo e fluidez.

**P: O histórico de downloads ou cache é armazenado?**  
R: Não. Todos os recursos são transmitidos diretamente ao dispositivo do usuário por meio de um proxy temporário; o servidor não armazena nenhuma solicitação ou arquivo de mídia.

**P: O que fazer se a análise falhar?**  
R: Por favor, verifique: ① Se o link corresponde a uma publicação pública válida ② Se sua conexão com a internet está estável ③ Tente com outro navegador. Se o problema persistir, não hesite em relatá-lo por meio de uma Issue.

---

## ⚖️ Conformidade regulatória e Isenção de responsabilidade

- Esta ferramenta **não contorna nem viola nenhuma medida de proteção técnica** das plataformas; limita-se a obter metadados por meio de interfaces públicas
- O usuário é responsável por verificar se seu uso está em conformidade com a legislação local e os termos de serviço da plataforma
- Casos de uso recomendados: Arquivamento pessoal, demonstrações educacionais, material de referência para criação de conteúdo... sempre dentro do marco do uso justo (Fair Use)
- Se identificar conteúdo que possa violar direitos, entre em contato com o canal oficial da [X por meio deste formulário de denúncia de direitos autorais](https://help.twitter.com/forms/dmca)

---

## 🤝 Guia de contribuição

Agradecemos suas Pull Requests e relatos de Issues! Antes de contribuir, por favor, consulte:
- [Padrões de código](/CONTRIBUTING.md)
- [Guia de tradução multilíngue](/locales/README.md)
- [Requisitos de segurança e conformidade](/SECURITY.md)

---

## 📄 Licença

Este projeto é publicado sob a [Licença MIT](/LICENSE). Pode ser utilizado gratuitamente para fins educacionais e de pesquisa. Para uso comercial, por favor, verifique cuidadosamente o cumprimento das regulamentações legais aplicáveis.

---

> 🌟 Se esta ferramenta foi útil para você, não hesite em ✨atribuir uma Estrela (Star)! Seu apoio é a maior motivação para continuarmos mantendo e melhorando este projeto~

*Última atualização: Maio de 2026 | Versão: v2.1.0*