---
title: Disponibilité des pilotes graphiques applicables sur Windows Update
description: La disponibilité de ces pilotes sur Windows Update (WU) détermine si un utilisateur est automatiquement invité à effectuer une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513463"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Disponibilité des pilotes graphiques applicables sur Windows Update

La disponibilité de ces pilotes sur Windows Update (WU) détermine si un utilisateur est automatiquement invité à effectuer une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10. Si des analyses matérielles ont montré qu’aucun pilote graphique n’était disponible sur Windows Update pour la carte graphique du PC, les utilisateurs n’ont pas fourni le système d’exploitation Windows 10 mis à jour. Toutefois, les utilisateurs peuvent toujours obtenir Windows 10 par le biais d’autres sources et effectuer manuellement la mise à niveau.

Certains utilisateurs n’ont pas été sûrs de la raison pour laquelle ils n’ont pas été mis à niveau lorsque d’autres personnes étaient, même si le conseiller de mise à niveau a expliqué qu’aucun pilote graphique n’était disponible pour leur matériel.

En outre, certains utilisateurs ont forcé une mise à niveau, puis ont découvert que leurs fonctionnalités graphiques et leurs performances ont été ralenties en raison de l’absence de pilote matériel.

## <a name="mitigations"></a>Corrections

Pour atténuer ce risque, les utilisateurs peuvent installer manuellement un ancien pilote, c.-à-d. à partir de Windows 7, Windows 8 ou Windows 8.1, en accédant au site Web IHV ou OEM et en téléchargeant un pilote de manière explicite. Cette opération doit être effectuée après la mise à niveau et n’est pas garantie. Aucune solution n’est prise en charge si aucun pilote graphique approprié n’est disponible sur WU. L’utilisateur doit décider s’il faut :

-   Rester sur le système d’exploitation précédent ;
-   Accepter les limitations du pilote logiciel, carte d’affichage de base Microsoft (MSBDA); ni
-   Achetez une nouvelle carte graphique disposant d’un pilote Windows 10 pris en charge.

## <a name="solutions"></a>Solutions

Il est essentiel que les IHV et les OEM chargent leurs pilotes graphiques Windows 10 dans WU pour tout matériel qu’ils envisagent de prendre en charge.

Notez que le matériel qui a atteint la fin de vie (EOL) peut ne pas avoir de pilotes sur WU. Il n’existe aucune solution dans ce cas : l’utilisateur doit choisir l’une des options sous atténuations ci-dessus.

 

 




