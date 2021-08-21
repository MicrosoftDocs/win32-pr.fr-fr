---
description: La propriété CostingComplete indique si le programme d’installation a terminé l’évaluation de l’espace disque.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propriété CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a512621e187be9897c07106ade8c6012d4ac4fa43543d71cb856e90027d549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948356"
---
# <a name="costingcomplete-property"></a>Propriété CostingComplete

La propriété **CostingComplete** indique si le programme d’installation a terminé l’évaluation de l’espace disque. Cette propriété peut être utilisée pour créer une boîte de dialogue déclenchée si le coût n’est pas terminé. La propriété est définie de façon dynamique lors de l’évaluation de l’espace disque et est définie sur 1 dès que le coût est terminé. Cette propriété est initialisée à 0 par l' [action CostFinalize](costfinalize-action.md).

## <a name="remarks"></a>Remarques

Pour obtenir un exemple illustrant comment créer un «Veuillez patienter. . . "boîte de dialogue qui s’affiche lors de l’évaluation de l’espace disque, consultez la section [création d’un conditionnel" Veuillez patienter... " MessageBox.](authoring-a-conditional-please-wait-------message-box.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




