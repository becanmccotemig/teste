# teste

```python
import subprocess

def executar_comando(comando):
    try:
        # Executa o comando e captura a saída
        resultado = subprocess.run(comando, shell=True, text=True, capture_output=True)
        
        # Verifica se o comando foi executado com sucesso
        if resultado.returncode == 0:
            print("Saída do comando:")
            print(resultado.stdout)
        else:
            print("Erro ao executar o comando:")
            print(resultado.stderr)
    except Exception as e:
        print(f"Ocorreu um erro: {e}")

# Exemplo de uso
comando = "ls -l"  # Comando para listar arquivos no diretório atual (no Linux/Mac) ou "dir" no Windows
executar_comando(comando)
```


