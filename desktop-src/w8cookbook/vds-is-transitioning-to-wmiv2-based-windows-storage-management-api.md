---
title: Le service de disque virtuel passe à l’API de gestion de stockage Windows
description: Le service de disque virtuel passe à l’API de gestion de stockage Windows
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383036"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Le service de disque virtuel passe à l’API de gestion de stockage Windows

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

À compter de Windows 8 et de Windows Server 2012, l’interface COM du service de disque virtuel est remplacée par l’API de gestion du stockage, une interface de programmation basée sur WMI. Pour la gestion des sous-systèmes de stockage (Windows), des partitions et des volumes, nous vous recommandons fortement d’utiliser l’API de gestion du stockage. Pour plus d’informations, consultez [API de gestion du stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Pour toutes les utilisations, à l’exception des volumes de démarrage miroir (à l’aide d’un volume miroir pour héberger le système d’exploitation), les disques dynamiques sont déconseillés. Pour les données qui nécessitent une résilience contre les défaillances de disque, utilisez des espaces de stockage, une solution de virtualisation de stockage résiliente. Pour plus d’informations, consultez [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Vous pouvez continuer à utiliser DiskPart, DiskRAID et la gestion des disques au cours de la période de dépréciation, mais ces outils ne fonctionnent pas avec les espaces de stockage ou avec les autres API de gestion de stockage Windows basées sur le nouveau Windows Management Instrumentation (WMI) ou les nouveaux utilitaires ou clients de gestion de stockage intégrés.


| API | Sous-systèmes de stockage | Disques de base | Disques dynamiques | Espaces de stockage |
| --- | --- | --- | --- | --- |
| VDS | Oui | Oui | Oui | Non |
| WMI | Oui | Oui | Non | Oui |
| DiskPart | n/a | Oui | Oui | Non |
| DiskRAID |  Oui | n/a | n/a | n/a |
| Interface utilisateur graphique de gestion des disques | n/a | Oui | Oui | Non |
| PowerShell | Oui | Oui | Non | Oui |
| Panneau de configuration espaces de stockage | n/a | Non | Non | Oui |


Le résultat de cette transition est l’augmentation de la résilience du stockage, de la disponibilité et de l’évolutivité. un langage de programmation et de script unifié, des coûts de gestion du stockage réduits et une gestion du stockage à distance plus facile.

## <a name="manifestation"></a>Manifestation

Les utilitaires DiskPart et DiskRAID utilisés dans l’environnement VDS ne prennent pas en charge les nouveaux espaces de stockage. De même, le nouvel utilitaire de stockage PowerShell ne prend pas en charge les disques dynamiques déconseillés

## <a name="mitigation"></a>Limitation des risques

Microsoft vous recommande vivement de baser les nouvelles applications de gestion du stockage sur l’API de gestion du stockage Windows et de faire passer les applications existantes basées sur l’infrastructure VDS à l’API de gestion du stockage Windows pendant vos cycles de mise à jour standard.

## <a name="resources"></a>Ressources

-   [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Applets de commande de stockage dans Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Windows Management Instrumentation](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 