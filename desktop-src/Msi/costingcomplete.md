---
description: La propriété CostingComplete indique si le programme d’installation a terminé l’évaluation de l’espace disque.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propriété CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522790"
---
# <a name="costingcomplete-property"></a>Propriété CostingComplete

La propriété **CostingComplete** indique si le programme d’installation a terminé l’évaluation de l’espace disque. Cette propriété peut être utilisée pour créer une boîte de dialogue déclenchée si le coût n’est pas terminé. La propriété est définie de façon dynamique lors de l’évaluation de l’espace disque et est définie sur 1 dès que le coût est terminé. Cette propriété est initialisée à 0 par l' [action CostFinalize](costfinalize-action.md).

## <a name="remarks"></a>Notes

Pour obtenir un exemple illustrant comment créer un «Veuillez patienter. . . "boîte de dialogue qui s’affiche lors de l’évaluation de l’espace disque, consultez la section [création d’un conditionnel" Veuillez patienter... " MessageBox.](authoring-a-conditional-please-wait-------message-box.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




