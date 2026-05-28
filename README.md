<h1 align="center"> GUSTAVO.EXE </h1>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?color=00FF00&size=24&center=true&vCenter=true&width=600&lines=Inicializando+sistema...;Carregando+Java...;Acesso+concedido.;Bem-vindo+ao+meu+GitHub" />
</p>

---

## 🖥️ SYSTEM.LOG

```bash
> user: Gustavo Rodrigues
> role: Dev em evolução
> focus: Java
> status: Aprendendo, evoluindo e criando
```

<p align="center"> <img src="https://streak-stats.demolab.com?user=Gustavo-Rodrigues1109&theme=chartreuse-dark&hide_border=true"/> </p>

name: generate animation

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the master branch
  push:
    branches:
    - master
    
  

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
          
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```bash
public static void main(String[] args) {
    System.out.println("> \"Evoluindo um commit por vez...");
}

> sistema continua em execução...
