# LABORATORIO 5
SESSÃO 6
karine@DESKTOP-83I35MU:~/incidente$ mkdir -p ~/relatorios/sessao6 && cd ~/relatorios/sessao6
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ echo '===== RELATÓRIO DE INCIDENTE — CVTECH Lda. =====' > relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  echo "Data: $(date)" >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ echo '--- CRONOLOGIA ---' >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ grep -E 'ERRO|monitor iniciado' ~/incidente/servidor.log >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ grep 'CPU normalizada' ~/incidente/servidor.log | head -n 1 >>
bash: syntax error near unexpected token `newline'
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ grep 'CPU normalizada' ~/incidente/servidor.log | head -n 1 >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ echo "Avisos registados: $(grep -c WARN ~/incidente/servidor.log)" >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ echo '--- PROCESSOS cvtech AINDA ATIVOS ---' >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ ps aux | grep '[c]vtech' >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  echo '--- TOP 5 DE CPU APÓS A INTERVENÇÃO ---' >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  ps aux --sort=-%cpu | head -n 6 >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  ps aux --sort=-%cpu | head -n 6 >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  ps aux --sort=-%cpu | head -n 6 >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$  ps aux --sort=-%cpu | head -n 6 >> relatorio_incidente.txt
karine@DESKTOP-83I35MU:~/relatorios/sessao6$ cat relatorio_incidente.txt
===== RELATÓRIO DE INCIDENTE — CVTECH Lda. =====
Data: Mon Oct 26 00:10:27 WET 2026
--- CRONOLOGIA ---
2026-10-25 22:39:12 INFO monitor iniciado
2026-10-25 22:39:12 ERRO cvtech-sync nÃ£o responde â€” CPU acima de 95%
2026-10-25 23:19:13 INFO CPU normalizada â€” cvtech-sync.sh terminado
Avisos registados: 938
--- PROCESSOS cvtech AINDA ATIVOS ---
--- TOP 5 DE CPU APÓS A INTERVENÇÃO ---
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
karine      7768  200  0.1   7292  4488 pts/0    R+   00:16   0:00 ps aux --sort=-%cpu
karine      7769  100  0.2  16304  7868 pts/0    S+   00:16   0:00 head -n 6
karine      7750  0.0  0.1   6212  5628 pts/0    S    00:13   0:00 bash
root         112  0.0  0.3  34636 11816 ?        Ss   Oct25   0:06 /usr/lib/systemd/systemd-udevd
root           1  0.0  0.4  24568 15504 ?        Ss   Oct25   0:04 /sbin/init
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
karine      7750  0.0  0.1   6212  5628 pts/0    S    00:13   0:00 bash
root         112  0.0  0.3  34636 11816 ?        Ss   Oct25   0:06 /usr/lib/systemd/systemd-udevd
root           1  0.0  0.4  24568 15504 ?        Ss   Oct25   0:04 /sbin/init
root          65  0.0  0.5  50656 20224 ?        S<s  Oct25   0:04 /usr/lib/systemd/systemd-journald
root         326  0.0  0.0   3880  1476 ?        S    Oct25   0:02 /init
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
karine      7772  100  0.1   7292  4488 pts/0    R+   00:16   0:00 ps aux --sort=-%cpu
karine      7773 50.0  0.2  16304  7832 pts/0    S+   00:16   0:00 head -n 6
karine      7750  0.0  0.1   6212  5628 pts/0    S    00:13   0:00 bash
root         112  0.0  0.3  34636 11816 ?        Ss   Oct25   0:06 /usr/lib/systemd/systemd-udevd
root           1  0.0  0.4  24568 15504 ?        Ss   Oct25   0:04 /sbin/init
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
karine      7750  0.0  0.1   6212  5628 pts/0    S    00:13   0:00 bash
root         112  0.0  0.3  34636 11816 ?        Ss   Oct25   0:06 /usr/lib/systemd/systemd-udevd
root           1  0.0  0.4  24568 15504 ?        Ss   Oct25   0:04 /sbin/init
root          65  0.0  0.5  50656 20224 ?        S<s  Oct25   0:04 /usr/lib/systemd/systemd-journald
root         326  0.0  0.0   3880  1476 ?        S    Oct25   0:02 /init
