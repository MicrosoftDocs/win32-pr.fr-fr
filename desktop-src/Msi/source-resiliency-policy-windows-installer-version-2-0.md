---
description: Windows La version 2,0 du programme d’installation commence à rechercher une source en vérifiant l’emplacement source utilisé le plus récemment dans la liste source, puis la liste des sources réseau, les sources de média et enfin les sources d’URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Stratégie de résilience source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951c1183da8998986863fe5dae744fc58c23387306c91153b50ab63e38e0a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039709"
---
# <a name="source-resiliency-policy"></a>Stratégie de résilience source

Le programme d’installation commence à rechercher une source en vérifiant l’emplacement source utilisé le plus récemment dans la liste source, puis la liste des sources réseau, les sources multimédias et enfin les sources d’URL. Pour plus d’informations, consultez [résilience source](source-resiliency.md). Si la recherche échoue, le programme d’installation peut présenter une [boîte de dialogue Parcourir](browse-dialog.md) permettant à l’utilisateur de rechercher la source manuellement. La boîte de dialogue Parcourir ne peut pas être affichée si les niveaux de l' [interface utilisateur](user-interface-levels.md) sont définis sur aucun. Un administrateur contrôle l’affichage de la boîte de dialogue Parcourir pour les utilisateurs en définissant la stratégie système.

avec Windows Installer, les non-administrateurs ne peuvent pas utiliser par défaut la boîte de dialogue parcourir pour localiser les sources d’applications gérées sur le média et ne peuvent pas installer les applications managées. Un administrateur permet à un non-administrateur de parcourir ou d’installer des applications gérées à partir d’un média à l’aide des stratégies [AllowLockdownBrowse](allowlockdownbrowse.md) et [AllowLockdownMedia](allowlockdownmedia.md) . Un administrateur désactive la possibilité de parcourir ou d’installer des applications à partir d’un média à l’aide des stratégies [DisAbleBrowse](disablebrowse.md) et [DisAbleMedia](disablemedia.md) .

le tableau suivant résume l’utilisation de ces stratégies système dans Windows Installer.



| Stratégie système                                  | Application non gérée par l’utilisateur non-administrateur                                                                                                             | Application non administrateur gérée par l’utilisateur                                                                                                                 | Application gérée non gérée par l’administrateur                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Les utilisateurs peuvent installer des applications non gérées à l’aide de sources situées sur le média. Les utilisateurs peuvent parcourir les supports pour rechercher les sources des applications non gérées.<br/>    | Les utilisateurs ne peuvent pas installer d’applications gérées à l’aide de sources situées sur le média. Les utilisateurs peuvent parcourir les supports pour rechercher les sources des applications gérées.<br/>      | Les administrateurs peuvent installer des applications à l’aide de sources situées sur des médias. Les administrateurs peuvent parcourir les médias pour rechercher les sources d’applications.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Les utilisateurs peuvent installer des applications non gérées à l’aide de sources situées sur le média. Les utilisateurs peuvent parcourir les supports pour rechercher les sources des applications non gérées.<br/>    | Les utilisateurs peuvent installer des applications gérées à l’aide de sources situées sur des médias. Les utilisateurs ne peuvent pas parcourir les supports pour les sources des applications gérées.<br/>      | Les administrateurs peuvent installer des applications à l’aide de sources situées sur des médias. Les administrateurs peuvent parcourir les médias pour rechercher les sources d’applications.<br/>    |
| *Par défaut*                                      | Les utilisateurs peuvent installer des applications non gérées à l’aide de sources situées sur le média. Les utilisateurs peuvent parcourir les supports pour rechercher les sources des applications non gérées.<br/>    | Les utilisateurs ne peuvent pas installer d’applications gérées à l’aide de sources situées sur le média. Les utilisateurs ne peuvent pas parcourir les supports pour les sources des applications gérées.<br/>   | Les administrateurs peuvent installer des applications à l’aide de sources situées sur des médias. Les administrateurs peuvent parcourir les médias pour rechercher les sources d’applications.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Les utilisateurs peuvent installer des applications non gérées à l’aide de sources situées sur le média. Les utilisateurs ne peuvent pas parcourir les supports pour les sources des applications non gérées.<br/> | Les utilisateurs ne peuvent pas installer d’applications gérées à l’aide de sources situées sur le média. Les utilisateurs ne peuvent pas parcourir les supports pour les sources des applications gérées. .<br/> | Les administrateurs peuvent installer des applications à l’aide de sources situées sur des médias. Les administrateurs ne peuvent pas parcourir les supports pour les sources des applications.<br/> |
| [DisAbleMedia](disablemedia.md)               | Les utilisateurs ne peuvent pas installer des applications non gérées à l’aide de sources situées sur le média. Les utilisateurs peuvent parcourir les supports pour rechercher les sources des applications non gérées.<br/> | Les utilisateurs ne peuvent pas installer d’applications gérées à l’aide de sources situées sur le média. Les utilisateurs ne peuvent pas parcourir les supports pour les sources des applications gérées.<br/>   | Les administrateurs ne peuvent pas installer d’applications à l’aide de sources situées sur le média. Les administrateurs peuvent parcourir les médias pour rechercher les sources d’applications.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 




