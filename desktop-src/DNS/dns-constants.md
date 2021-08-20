---
title: Constantes DNS
description: Les constantes suivantes sont définies pour DNS dans l’ordre d’octet de l’hôte.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61da11c9d8f5af28e2152bad5fe9c7b5eb6eb7d83fdb7f94c11e8c2f3c04d9f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164155"
---
# <a name="dns-constants"></a>Constantes DNS

Les constantes suivantes sont définies pour DNS dans l’ordre d’octet de l’hôte.

## <a name="dns-record-types"></a>Types d’enregistrements DNS



| Constante           | Valeur            |
|--------------------|------------------|
| \_type \_ de DNS A       | 0x0001           |
| \_type DNS \_ NS      | 0x0002           |
| \_type DNS \_ MD      | 0x0003           |
| \_type DNS \_ MF      | 0x0004           |
| \_CNAME de type DNS \_   | 0x0005           |
| \_type DNS \_ SOA     | 0x0006           |
| \_type DNS \_ MB      | 0x0007           |
| \_type DNS \_ mg      | 0x0008           |
| \_type DNS \_ Mr      | 0x0009           |
| \_type DNS \_ null    | 0x000a           |
| TYPE de DNS \_ \_ WKS     | 0x000b           |
| \_ptr de type DNS \_     | 0x000c           |
| TYPE de DNS \_ \_ HINFO   | 0x010E           |
| \_type DNS \_ minfo   | 0x000e           |
| \_type DNS \_ MX      | 0x000F           |
| \_texte de type DNS \_    | 0x0010           |
| \_type DNS \_ RP      | 0x0011           |
| TYPE de DNS \_ \_ AFSDB   | 0x0012           |
| TYPE de DNS \_ \_ x.25     | 0x0013           |
| TYPE de DNS \_ \_ RNIS    | 0x0014           |
| TYPE de DNS \_ \_ RT      | 0x0015           |
| TYPE de DNS \_ \_ NSAP    | 0x0016           |
| \_NSAPPTR de type DNS \_ | 0x0017           |
| \_SIG de type DNS \_     | 0x0018           |
| \_clé de type DNS \_     | 0x0019           |
| \_type DNS \_ PX      | 0x001a           |
| \_objets de stratégie de groupe de type DNS \_    | 0x011C           |
| \_type DNS \_ aaaa    | 0x011B           |
| \_loc de type DNS \_     | 0x011E           |
| TYPE de DNS \_ \_ NXT     | 0x011D           |
| \_eID du type DNS \_     | 0x001f           |
| \_NIMLOC de type DNS \_  | 0x0020           |
| \_SRV de type DNS \_     | 0x0021           |
| TYPE de DNS \_ \_ ATMA    | 0x0022           |
| \_NAPTR de type DNS \_   | 0x0023           |
| \_Kx de type DNS \_      | 0x0024           |
| \_certificat de type DNS \_    | 0x0025           |
| \_Type DNS \_ a6      | 0x0026           |
| \_type DNS \_ dname   | 0x0027           |
| \_récepteur de type DNS \_    | 0x0028           |
| \_type DNS \_ opt     | 0x0029           |
| \_DS de type DNS \_      | 0x002B           |
| \_RRSIG de type DNS \_   | 0x002E           |
| TYPE de DNS \_ \_ NSEC    | 0x002F           |
| \_DNSKEY de type DNS \_  | 0x0030           |
| \_DHCID de type DNS \_   | 0x0031           |
| \_UINFO de type DNS \_   | 0x0064           |
| \_UID de type DNS \_     | 0x0065           |
| \_GID de type DNS \_     | 0x0066           |
| TYPE DNS non \_ \_ spec  | 0x0067           |
| \_ADR de type DNS \_   | 0x00f8           |
| \_type DNS \_ TKey    | 0x00f9           |
| TYPE de DNS \_ \_ TSIG    | 0x00fa           |
| \_type DNS \_ IXFR    | 0x00fb           |
| TYPE de DNS \_ \_ AXFR    | 0x00fc           |
| \_mailb de type DNS \_   | 0x00fd           |
| \_messagerie de type DNS \_   | 0x00fe           |
| \_type DNS \_ tout     | 0x00ff           |
| \_type DNS \_ any     | 0x00ff           |
| \_type DNS \_ WINS    | 0xff01           |
| \_ \_ WINSR type DNS   | 0xff02           |
| \_type DNS \_ NBSTAT  | \_ \_ WINSR type DNS |



 

## <a name="dns-class-types"></a>Types de classe DNS



| Constante             | Valeur  |
|----------------------|--------|
| \_classe DNS \_ Internet | 0x0001 |
| \_CSNET de classe DNS \_    | 0x0002 |
| \_chaos de classe DNS \_    | 0x0003 |
| \_HESIOD de classe DNS \_   | 0x0004 |
| \_classe DNS \_ aucun     | 0x00fe |
| \_classe DNS \_ tout      | 0x00ff |
| \_classe DNS \_ any      | 0x00ff |



 

## <a name="dns-query-types"></a>Types de requêtes DNS



| Constante                    | Valeur  |
|-----------------------------|--------|
| \_requête OPCODE \_ DNS          | 0x0000 |
| l' \_ OPCODE DNS \_ IQueryable         | 0x0001 |
| \_État du \_ serveur \_ OPCODE DNS | 0x0002 |
| \_OPCODE DNS \_ inconnu        | 0x0003 |
| \_notification OPCODE \_ DNS         | 0x0004 |
| \_ \_ mise à jour de l’OPCODE DNS         | 0x0005 |



 

## <a name="dns-record-flags"></a>Indicateurs d’enregistrement DNS

Les indicateurs suivants font référence à la section d’un enregistrement de ressource (RR) dans un message DNS :



| Constante           | Valeur      | Signification                         |
|--------------------|------------|---------------------------------|
| \_question DNSREC   | 0x00000000 | Le RR est dans la section de question   |
| \_réponse DNSREC     | 0x00000001 | Le RR est dans la section de réponse     |
| \_autorité DNSREC  | 0x00000002 | Le RR est dans la section autorité  |
| DNSREC \_ supplémentaires | 0x00000003 | Le RR est dans la section supplémentaire |



 

Les indicateurs suivants font référence à la section d’un RR dans un message de mise à jour DNS par [RFC 2136](https://www.ietf.org/rfc/rfc2136.txt):



| Constante       | Valeur      | Signification                           |
|----------------|------------|-----------------------------------|
| \_zone DNSREC   | 0x00000000 | Le RR est dans la section zone         |
| DNSREC \_ PREREQ | 0x00000001 | Le RR est dans la section conditions préalables |
| \_mise à jour DNSREC | 0x00000002 | Le RR est dans la section Update       |



 

Les indicateurs suivants s’excluent mutuellement :



| Constante        | Valeur      | Signification                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ Supprimer  | 0x00000004 | Supprimer un RR. Utilisé conjointement avec la \_ mise à jour DNSREC       |
| DNSREC \_ NOexist | 0x00000004 | Le RR n’existe pas. Utilisé conjointement avec DNSREC \_ PREREQ |



 

## <a name="dns-query-options"></a>Options de requête DNS



| Constante                                | Valeur      | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_norme de requête DNS \_                    | 0x00000000 | Requête standard.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_ \_ \_ réponse tronquée d’acceptation de la requête DNS \_ | 0x00000001 | Retourne des résultats tronqués. N’effectue pas de nouvelle tentative sous TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| la \_ requête DNS \_ utilise \_ TCP \_ uniquement              | 0x00000002 | Utilise TCP uniquement pour la requête.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_requête DNS \_ aucune \_ récursivité               | 0x00000004 | Indique au serveur DNS d’effectuer une requête itérative (en particulier, il demande au serveur DNS de ne pas effectuer de résolution récursive pour résoudre la requête).                                                                                                                                                                                                                                                                                                   |
| \_cache de \_ contournement de requêtes DNS \_               | 0x00000008 | Contourne le cache de [*résolution*](r-gly.md) sur la recherche.                                                                                                                                                                                                                                                                                                                                                                            |
| requête DNS- \_ \_ aucune \_ requête de câble \_             | 0x00000010 | Indique à DNS d’exécuter uniquement une requête sur le cache local. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge. Pour une fonctionnalité similaire, **Utilisez \_ \_ \_ uniquement le cache de requête DNS**.<br/>                                                                                                                                                                                                                                      |
| \_ \_ \_ nom local de la requête DNS \_             | 0x00000020 | Indique à DNS d’ignorer le nom local. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_fichier de requête DNS \_ sans \_ hôte \_             | 0x00000040 | Empêche la requête DNS de consulter le fichier HOSTs. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                   |
| \_requête DNS \_ non \_ NetBT                   | 0x00000080 | Empêche la requête DNS d’utiliser NetBT pour résoudre le problème. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                  |
| \_câble de requête DNS \_ \_ uniquement                  | 0x00000100 | Indique à DNS d’exécuter une requête à l’aide du réseau uniquement, en ignorant les informations locales. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                      |
| MESSAGE de retour de la \_ requête DNS \_ \_             | 0x00000200 | Indique à DNS de renvoyer l’intégralité du message de réponse DNS. **Windows 2000 Server et Windows 2000 Professional :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                   |
| multidiffusion des \_ requêtes DNS \_ \_ uniquement             | 0x00000400 | Empêche la requête d’utiliser DNS et utilise uniquement LLMNR (Link multicast Name Resolution). **Windows Vista et Windows Server 2008 ou version ultérieure. :** Cette valeur est prise en charge.<br/>                                                                                                                                                                                                                                                                  |
| \_requête DNS \_ sans \_ multidiffusion               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_traitement de la requête DNS \_ \_ en tant que \_ nom de domaine complet             | 0x00001000 | Empêche la réponse DNS de joindre des suffixes au nom envoyé dans un processus de résolution de noms.                                                                                                                                                                                                                                                                                                                                                  |
| \_ADDRCONFIG de requête DNS \_                  | 0x00002000 | Windows 7 uniquement : n’envoyez pas [**de requêtes de**](/windows/win32/api/windns/ns-windns-dns_a_data) type si les adresses IPv4 ne sont pas disponibles sur une interface et n’envoient pas de requêtes de type [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) si les adresses IPv6 ne sont pas disponibles.                                                                                                                                                                                                                                   |
| \_ \_ adresse double d’une requête DNS \_                  | 0x00004000 | Windows 7 uniquement : interrogez les enregistrements [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) et [**de**](/windows/win32/api/windns/ns-windns-dns_a_data) type et retournent des résultats pour chacun. Les résultats d' **un** enregistrement de type sont mappés au type **aaaa** .                                                                                                                                                                                                                                                           |
| attente de la \_ multidiffusion des requêtes DNS \_ \_             | 0x00020000 | Attend un délai d’attente complet pour collecter toutes les réponses du lien local. Si la valeur n’est pas définie, le comportement par défaut consiste à retourner avec la première réponse. **Windows Vista et Windows Server 2008 ou version ultérieure. :** Cette valeur est prise en charge.<br/>                                                                                                                                                                                                              |
| vérification de la \_ multidiffusion des requêtes DNS \_ \_           | 0x00040000 | Dirige un test à l’aide du nom d’hôte de l’ordinateur local pour vérifier l’unicité du nom sur le même lien local. Collecte toutes les réponses, même si le comportement normal de l’expéditeur LLMNR n’est pas activé. **Windows Vista et Windows Server 2008 ou version ultérieure. :** Cette valeur est prise en charge.<br/>                                                                                                                                                                                  |
| les valeurs TTL de la requête DNS ne sont pas \_ \_ \_ réinitialisées \_ \_    | 0x00100000 | Si la valeur est définie et si la réponse contient plusieurs enregistrements, les enregistrements sont stockés avec la durée de vie correspondant à la durée de vie de valeur minimale parmi tous les enregistrements. Lorsque cette option est définie, la valeur « ne pas modifier la durée de vie des enregistrements individuels » dans le jeu d’enregistrements retourné n’est pas modifiée.                                                                                                                                                                               |
| \_encodage \_ IDN de désactivation des requêtes DNS \_ \_      | 0x00200000 | Désactive la prise en charge de l’encodage IDN (International Domain Name) dans les API [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**DnsQueryEx**](/windows/desktop/api/Windns/nf-windns-dnsqueryex), [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)et [**DnsReplaceRecordSet**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) . Tous les noms Punycode sont traités comme des caractères ASCII et sont encodés en ASCII sur le câble. Tous les noms non-ASCII sont encodés en UTF8 sur le câble. **Windows 8 ou version ultérieure. :** Cette valeur est prise en charge.<br/> |
| ajout de la requête DNS sur les \_ \_ \_ étiquettes          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_requête DNS \_ réservée                    | 0xf0000000 | Réservé.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Options de mise à jour DNS



| Constante                                 | Valeur      | Signification                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sécurité des mises à jour DNS \_ \_ \_ par défaut      | 0x00000000 | Utilise le comportement par défaut, qui est spécifié dans le registre, pour les mises à jour DNS dynamiques sécurisées.                                                                |
| \_sécurité des mises à jour DNS \_ \_ désactivée               | 0x00000010 | N’essaie pas les mises à jour dynamiques sécurisées.                                                                                                                      |
| \_sécurité des mises à jour DNS \_ \_ sur                | 0x00000020 | Tente une mise à jour dynamique non sécurisée ; en cas de refus, tente de sécuriser la mise à jour dynamique.                                                                               |
| \_sécurité des mises à jour DNS \_ \_ uniquement              | 0x00000100 | Tente uniquement de sécuriser les mises à jour dynamiques.                                                                                                                         |
| \_contexte de \_ sécurité du cache des mises à jour DNS \_ \_    | 0x00000200 | Met en cache le contexte de sécurité pour une utilisation dans de futures transactions.                                                                                                   |
| \_test de mise à jour DNS \_ utiliser un \_ \_ \_ compte sys local \_ | 0x00000400 | Utilise les informations d’identification du compte d’ordinateur local.                                                                                                               |
| Nego de la sécurité des \_ mises à jour DNS \_ \_ \_       | 0x00000800 | N’utilise pas le contexte de sécurité mis en cache.                                                                                                                         |
| \_mise à jour DNS \_ essayer \_ tous les \_ \_ serveurs maîtres   | 0x00001000 | Envoie les mises à jour DNS à tous les serveurs DNS à plusieurs maîtres.                                                                                                            |
| \_mise à jour DNS \_ Ignorer les \_ \_ adaptateurs de mise à jour \_  | 0x00002000 | Ne mettez pas à jour les adaptateurs où les mises à jour DNS dynamiques sont désactivées. **Windows serveur 2000 avec SP2 ou version ultérieure. :** Cette valeur est prise en charge.<br/>                 |
| \_serveur distant de mise à jour DNS \_ \_              | 0x00004000 | Inscrire des enregistrements CNAMe sur un serveur distant en plus du serveur DNS local. **Windows serveur 2000 avec SP2 ou version ultérieure. :** Cette valeur est prise en charge.<br/> |
| \_mise à jour DNS \_ réservée                    | 0xffff0000 | Réservé pour un usage futur.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Codes de réponse DNS



| Erreur                | Signification                                        |
|----------------------|------------------------------------------------|
| \_erreur DNS RCODE \_  | Aucune erreur                                       |
| \_ancien RCODE \_ DNS  | Erreur de format                                   |
| \_SERVFAIL RCODE \_ DNS | Défaillance du serveur                                 |
| \_RCODE DNS \_ | Erreur de nom                                     |
| \_NOTIMPL RCODE \_ DNS  | Non implémenté                                |
| \_RCODE DNS \_ refusé  | Connexion refusée                             |
| \_YXDOMAIN RCODE \_ DNS | Le nom de domaine ne doit pas exister                   |
| \_YXRRSET RCODE \_ DNS  | Le jeu d’enregistrements de ressources (RR) ne doit pas exister      |
| \_NXRRSET RCODE \_ DNS  | L’ensemble de RR n’existe pas                          |
| \_NOTAUTH RCODE \_ DNS  | Ne fait pas autorité pour la zone                     |
| \_NOTZONE RCODE \_ DNS  | Le nom n’est pas dans la zone                               |
| \_BADVERS RCODE \_ DNS  | Mécanisme d’extension incorrect pour la version DNS (EDNS) |
| \_BADSIG RCODE \_ DNS   | Signature incorrecte                                  |
| \_BADKEY RCODE \_ DNS   | Clé incorrecte                                        |
| \_BADTIME RCODE \_ DNS  | Horodatage incorrect                                  |



 

 

 





