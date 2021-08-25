---
title: disponibilité des pilotes graphiques applicables sur Windows Update
description: la disponibilité de ces pilotes sur Windows Update (WU) détermine si une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10 est automatiquement proposée à l’utilisateur.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 906894f317a86d851501e913e3c9491dc1f83336f7f80eefa660ee43d3510b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935429"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>disponibilité des pilotes graphiques applicables sur Windows Update

la disponibilité de ces pilotes sur Windows Update (WU) détermine si une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10 est automatiquement proposée à l’utilisateur. si des analyses matérielles ont montré qu’aucun pilote graphique n’était disponible sur Windows Update pour la carte graphique du PC, les utilisateurs n’ont pas fourni le système d’exploitation Windows 10 mis à jour. toutefois, les utilisateurs peuvent toujours obtenir des Windows 10 par le biais d’autres sources et effectuer manuellement la mise à niveau.

certains utilisateurs n’ont pas été sûrs de la raison pour laquelle ils n’ont pas proposé la mise à niveau lorsque d’autres personnes étaient, même si le Conseiller de mise à niveau expliqué qu’aucun pilote graphique n’était disponible pour leur matériel.

En outre, certains utilisateurs ont forcé une mise à niveau, puis ont découvert que leurs fonctionnalités graphiques et leurs performances ont été ralenties en raison de l’absence de pilote matériel.

## <a name="mitigations"></a>Corrections

pour atténuer ce risque, les utilisateurs peuvent installer manuellement un ancien pilote, c.-à-d. Windows 7, Windows 8 ou Windows 8.1, en accédant au site web IHV ou OEM et en téléchargeant un pilote de manière explicite. Cette opération doit être effectuée après la mise à niveau et n’est pas garantie. Aucune solution n’est prise en charge si aucun pilote graphique approprié n’est disponible sur WU. L’utilisateur doit décider s’il faut :

-   Rester sur le système d’exploitation précédent ;
-   Accepter les limitations du pilote logiciel, carte d’affichage de base Microsoft (MSBDA); ni
-   achetez une nouvelle carte graphique disposant d’un pilote Windows 10 pris en charge.

## <a name="solutions"></a>Solutions

il est essentiel que les ihv et les oem chargent leurs pilotes graphiques Windows 10 dans WU pour tout matériel qu’ils envisagent de prendre en charge.

Notez que le matériel qui a atteint la fin de vie (EOL) peut ne pas avoir de pilotes sur WU. Il n’existe aucune solution dans ce cas : l’utilisateur doit choisir l’une des options sous atténuations ci-dessus.

 

 




