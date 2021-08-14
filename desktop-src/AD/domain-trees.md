---
title: Arborescences de domaines
description: Une arborescence de domaine est constituée de plusieurs domaines qui partagent un schéma et une configuration communs, formant un espace de noms contigu.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory de l’arborescence de domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a1e2ed05284d2a08735b048fb41d97d6597634f711094d0a3763c2d7f8be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430513"
---
# <a name="domain-trees"></a>Arborescences de domaines

Une *arborescence de domaine* est constituée de plusieurs domaines qui partagent un schéma et une configuration communs, formant un espace de noms contigu. Les domaines d’une arborescence sont également liés par des relations d’approbation. Active Directory est un ensemble d’une ou plusieurs arborescences.

Les arborescences peuvent être consultées de deux façons. Une vue est celle des relations d’approbation entre les domaines. L’autre vue est l’espace de noms de l’arborescence de domaine.

## <a name="viewing-trust-relationships"></a>Affichage des relations d’approbation

Vous pouvez dessiner un diagramme d’une arborescence de domaine en fonction des domaines individuels et de la relation d’approbation existante.

Windows 2000 établit des relations d’approbation entre des domaines basés sur le protocole de sécurité Kerberos. L’approbation Kerberos est transitive et hiérarchique : si le domaine A approuve le domaine B et que le domaine B approuve le domaine C, le domaine A approuve le domaine C.

![relation d’approbation de l’arborescence de domaine](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Affichage de l’espace de noms

Vous pouvez également dessiner un diagramme d’une arborescence de domaine en fonction de l’espace de noms. Vous pouvez déterminer le nom unique d’un objet en suivant le chemin d’accès vers le haut de la hiérarchie de l’espace de noms de l’arborescence de domaine. Cette vue est utile pour regrouper des objets dans une hiérarchie logique. Le principal avantage d’un espace de noms contigu est qu’une recherche profonde depuis la racine de l’espace de noms recherche dans l’ensemble de la hiérarchie.

![arborescence du domaine de l’espace de noms](images/namespace.png)

 

 




