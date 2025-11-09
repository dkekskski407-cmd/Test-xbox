Script Box - Projeto UWP pronto para build (ScriptBox)
===================================================

Conteúdo
- Pasta 'ScriptBox' contém o projeto UWP (código fonte).
- Solution 'ScriptBox.sln' para abrir no Visual Studio.
- Package.appxmanifest já preenchido com DisplayName 'Script Box'.

Como gerar o .appx (passos no seu Windows com Visual Studio):
1. Abra `ScriptBox.sln` no Visual Studio 2019/2022.
2. Restaure pacotes NuGet (Menu: Tools -> NuGet Package Manager -> Restore).
3. Selecione 'Release' e plataforma 'x64' no topo do Visual Studio.
4. Vá em Project -> Store -> Create App Packages... (ou Project -> Publish -> Create App Packages).
   - Escolha "Sideloading" / "No" para Store.
5. Siga o assistente e gere o pacote `.appx` ou `.msixbundle`.
6. Para instalar no Xbox Dev Mode:
   - Ative Dev Mode no Xbox e abra Device Portal.
   - Em Device Portal -> Apps -> Install app, faça upload do `.appx` e do certificado (se solicitado).
   - Caso precise, gere um certificado autoassinado em Visual Studio (Create test certificate).
Observações:
- O projeto usa MoonSharp (MoonSharp.Interpreter) gerenciado; não há binários nativos.
- Se quiser, posso gerar um certificado de desenvolvedor e instruções passo-a-passo para assinar o pacote.
