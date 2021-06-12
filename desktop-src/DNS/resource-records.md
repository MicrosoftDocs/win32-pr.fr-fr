---
title: Enregistrements de ressources
description: En savoir plus sur les enregistrements de ressources. Un enregistrement de ressource est l’unité d’entrée d’informations dans les fichiers de zone DNS, qui permet de résoudre toutes les requêtes DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010672"
---
# <a name="resource-records"></a>Enregistrements de ressources

Un enregistrement de ressource, communément appelé RR, est l’unité d’entrée d’informations dans les fichiers de zone DNS. Les RR sont les blocs de construction de base des informations IP et de nom d’hôte et sont utilisés pour résoudre toutes les requêtes DNS. Les enregistrements de ressources existent sous la forme de plusieurs types pour fournir des services de résolution de noms étendus.

Les différents types de RR ont des formats différents, car ils contiennent des données différentes. En général, toutefois, de nombreux RR partagent un format commun, comme l’illustre l’exemple d’enregistrement de ressource d’adresse suivant. L’exemple fictif suivant explique les champs trouvés dans un enregistrement de ressource A :

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   Le premier champ (microsoft.com) indique le propriétaire.
-   Le deuxième champ (600) est le paramètre de durée de vie (TTL, Time-to-Live), en secondes.
-   Le troisième champ (dans) est le champ de classe qui représente la famille de protocoles, qui est presque toujours dans, pour la classe Internet.
-   Le quatrième champ (A) est le type de ressource que le RR représente.
-   Le cinquième champ (150.150.150.1) est les données de ressource, ou RDATA. Ce champ est un type de variable qui fournit des informations appropriées pour le type de ressource ; dans ce cas, il s’agit d’une adresse IP 32 bits.

Les types d’enregistrements de ressources suivants sont couramment utilisés dans DNS :

-   SOA (Start of Authority)
-   Serveur de noms (NS)
-   [*Enregistrement de pointeur*](p-gly.md) (PTR)
-   Adresse (A)
-   Adresse IPv6 (AAAA)
-   Exchange mail (MX)
-   [*Nom canonique*](c-gly.md) (CNAME)
-   Windows Internet Service de nommage (WINS)
-   Recherche inversée WINS (WINSr)

Il existe de nombreux autres types d’enregistrements de ressources dans DNS. Pour plus d’informations, consultez [Référence du fournisseur WMI DNS](dns-wmi-provider-reference.md).

 

 




