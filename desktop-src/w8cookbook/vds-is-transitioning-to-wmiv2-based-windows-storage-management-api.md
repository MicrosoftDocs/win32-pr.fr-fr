---
title: le Service disque virtuel est en train de passer à Windows API de gestion Stockage
description: le Service disque virtuel est en train de passer à Windows API de gestion Stockage
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45e25452ae0b6bb20e0ca04130b7fa2fd64f2a191d504380f973f663b7931ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852036"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>le Service disque virtuel est en train de passer à Windows API de gestion Stockage

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

à partir de Windows 8 et Windows Server 2012, l’interface COM du Service de disque virtuel est remplacée par l’API de gestion des Stockage, une interface de programmation basée sur WMI. pour la gestion des sous-systèmes de stockage, (Windows) des disques, des partitions et des volumes, nous vous recommandons fortement d’utiliser l’API de gestion des Stockage. pour plus d’informations, consultez [Windows Stockage API de gestion](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Pour toutes les utilisations, à l’exception des volumes de démarrage miroir (à l’aide d’un volume miroir pour héberger le système d’exploitation), les disques dynamiques sont déconseillés. pour les données qui nécessitent une résilience contre les défaillances de disque, utilisez espaces de stockage, une solution de virtualisation de stockage résiliente. pour plus d’informations, consultez [espaces de stockage Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

vous pouvez continuer à utiliser DiskPart, DiskRAID et la gestion des disques au cours de la période de dépréciation, mais ces outils ne fonctionnent pas avec espaces de stockage ou avec d’autres api de gestion de Stockage Windows basées sur le Windows Management Instrumentation (WMI) ou des utilitaires de gestion de stockage intégrés ou des clients.


| API | Sous-systèmes de stockage | Disques de base | Disques dynamiques | Espaces de stockage |
| --- | --- | --- | --- | --- |
| VDS | Oui | Oui | Oui | Non |
| WMI | Oui | Oui | Non | Oui |
| DiskPart | n/a | Oui | Oui | Non |
| DiskRAID |  Oui | n/a | n/a | n/a |
| Interface utilisateur graphique de gestion des disques | n/a | Oui | Oui | Non |
| PowerShell | Oui | Oui | Non | Oui |
| espaces de stockage Panneau de configuration | n/a | Non | Non | Oui |


Le résultat de cette transition est l’augmentation de la résilience du stockage, de la disponibilité et de l’évolutivité. un langage de programmation et de script unifié, des coûts de gestion du stockage réduits et une gestion du stockage à distance plus facile.

## <a name="manifestation"></a>Manifestation

les utilitaires DiskPart et DiskRAID utilisés dans l’environnement VDS ne prennent pas en charge la nouvelle espaces de stockage. de même, le nouvel utilitaire PowerShell Stockage ne prend pas en charge les disques dynamiques déconseillés

## <a name="mitigation"></a>Limitation des risques

Microsoft vous recommande vivement de baser les nouvelles applications de gestion du stockage sur l’api de gestion de l’Windows Stockage, et de faire passer les applications existantes basées sur l’infrastructure VDS à l’api de gestion des Stockage Windows lors de vos cycles de mise à jour standard.

## <a name="resources"></a>Ressources

-   [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Applets de commande de stockage dans Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Windows Management Instrumentation](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 