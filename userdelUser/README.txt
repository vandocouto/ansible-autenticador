Para deletar um usuario, vána task userdel.yml e insira o nome do usuario que deseja deletar.

Exemplo: 

Deletando o usuario evandro.couto de todos os hosts que foram informados no invetory.

# vim user_del/tasks/userdel.yml

---
- name: "Removendo os usuarios"
  user: name={{item}} state=absent remove=yes
  with_items:
   - evandro.couto

