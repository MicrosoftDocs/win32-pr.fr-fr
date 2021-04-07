---
title: Serveurs Active Directory et DNS dynamique
description: Les serveurs Active Directory publient leurs adresses afin que les clients puissent les trouver en connaissant uniquement le nom de domaine.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671014"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Serveurs Active Directory et DNS dynamique

Les serveurs Active Directory publient leurs adresses afin que les clients puissent les trouver en connaissant uniquement le nom de domaine. Les serveurs Active Directory sont publiés à l’aide des enregistrements de ressource de service (RR SRV) dans DNS. Le RR SRV est un enregistrement DNS utilisé pour mapper le nom d’un service à l’adresse d’un serveur qui offre le service. Le nom d’un enregistrement de ressource SRV se présente sous la forme suivante :


```C++
<service>.<protocol>.<domain>
```



Les serveurs Active Directory offrent le service LDAP sur le protocole TCP afin que les noms publiés soient « LDAP. TCP <domain> ». Par conséquent, l’enregistrement de ressource SRV pour fabrikam.com est « ldap.tcp.fabrikam.com ». Des données supplémentaires sur le RR SRV indiquent la priorité et le poids du serveur, ce qui permet aux clients de choisir le serveur le mieux adapté à leurs besoins.

Lorsqu’un serveur Active Directory est installé, il utilise le DNS dynamique pour se publier lui-même. Étant donné que les adresses TCP/IP sont sujettes à modification, les serveurs vérifient périodiquement leurs inscriptions pour s’assurer qu’elles sont correctes et les mettent à jour si nécessaire.

Le DNS dynamique est un ajout récent à la norme DNS. Le DNS dynamique définit un protocole pour la mise à jour dynamique d’un serveur DNS avec de nouvelles données. Avant le DNS dynamique, les administrateurs devaient configurer manuellement les enregistrements stockés par les serveurs DNS.

 

 




