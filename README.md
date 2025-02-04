# SAE3.01B

## Régles de pare-feu

- [x] La résolution de nom est dirigié par le `pc_dns`, situé dans le réseau de `r_s`.

- [x] Ping (ICMP) : `r_dsi` doit pouvoir faire des pings à toutes les machines dans l'infrastructure

- [x] Les patients (`r_p`) et visiteurs (`r_v`) doivent avoir accès au `pc_s` pour pouvoir accéder au site web publique
- [x] Les patients (`r_p`) et visiteurs (`r_v`) doivent avoir accès à Internet, via `r_0`

- [x] Les étudiants (`r_etu`) et les enseignants (`r_ens`) doivent avoir accès au `pc_mail` pour pouvoir accéder à leur boîte mail
- [x] Les étudiants (`r_etu`) et les enseignants (`r_ens`) doivent avoir accès au `pc_s` pour pouvoir accéder au site web publique **et** interne
- [x] Les étudiants (`r_etu`) et les enseignants (`r_ens`) doivent avoir accès à Internet, via `r_0`

- [x] Les chercheurs (`r_c`) et les enseignants-chercheurs (`r_ec`) doivent avoir accès au `pc_mail` pour pouvoir accéder à leur boîte mail
- [x] Les chercheurs (`r_c`) et les enseignants-chercheurs (`r_ec`) doivent avoir accès au `pc_s` pour pouvoir accéder au site web publique **et** interne
- [x] Les chercheurs (`r_c`) et les enseignants-chercheurs (`r_ec`) doivent avoir accès à Internet, via `r_0`
- [x] Les chercheurs (`r_c`) et les enseignants-chercheurs (`r_ec`) doivent avoir accès à `pc_bdd` en SFTP

- [x] Le personnel soignant (`r_ps`) doit avoir accès au `pc_mail` pour pouvoir accéder à leur boîte mail
- [x] Le personnel soignant (`r_ps`) doit avoir accès au `pc_s` pour pouvoir accéder au site web publique, interne et application de RDV (disponible sur `TCP/1224`)
- [x] Le personnel soignant (`r_ps`) doit avoir accès à Internet, via `r_0`

- [x] La comptabilité (`r_ct`) doit avoir accès au `pc_mail` pour pouvoir accéder à leur boîte mail
- [x] La comptabilité (`r_ct`) doit avoir accès au `pc_s` pour pouvoir accéder au site web publique et à l'application de gestion de RDV (disponible sur `TCP/1224`) pour le suivi financier
- [x] La comptabilité (`r_ct`) doit avoir accès à Internet, via `r_0`

- [x] La DSI (`r_dsi`) (sauf `pc_bdd`) doit avoir accès à tout les services, machines et Internet
- [x] Le RSSI (`pc_rssi`) doit pouvoir accéder à tout les services, machines (y compris `pc_bdd`) et Internet

## Tester les règles de pare-feu

Sur chaque machine, exécuter la commande suivante :

```bash
chmod +x /shared/testing/test.sh && /shared/testing/test.sh
```
