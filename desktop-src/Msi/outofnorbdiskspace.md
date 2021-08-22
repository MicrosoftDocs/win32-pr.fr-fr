---
description: Le programme d’installation définit la propriété OutOfNoRbDiskSpace sur true si un volume qui est une cible de l’installation ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propriété OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275eec4c78a1fe0074fe8e91f7dcab3b660cade46eb8810aa992edf6a45fb989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942769"
---
# <a name="outofnorbdiskspace-property"></a>Propriété OutOfNoRbDiskSpace

Le programme d’installation définit la propriété **OutOfNoRbDiskSpace** sur true si un volume qui est une cible de l’installation ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation. Dans ce cas, la propriété **OutOfNoRbDiskSpace** est définie sur true même si la restauration a été désactivée. Si tous les volumes disposent de suffisamment d’espace, la valeur est false.

Un développeur d’un package d’installation peut gérer la situation lorsque la propriété [**OutOfDiskSpace**](outofdiskspace.md) a la valeur true et que la propriété **OutOfNoRbDiskSpace** a la valeur false en créant une interface utilisateur qui présente à l’utilisateur une option permettant de désactiver la restauration et de poursuivre l’installation. Pour plus d’informations sur l’affichage conditionnel d’une boîte de dialogue, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md). Pour plus d’informations sur la désactivation de la restauration, consultez [EnableRollback ControlEvent,](enablerollback-controlevent.md).

La propriété **OutOfNoRbDiskSpace** est valide à tout moment après l’exécution de l' [action CostFinalize](costfinalize-action.md) . L’état de la propriété **OutOfNoRbDiskSpace** est mis à jour de manière dynamique chaque fois que le coût total d’installation est recalculé (par exemple, chaque fois que l’état d’installation d’une fonctionnalité est modifié via la [boîte de dialogue de sélection](selection-dialog.md)). Les actions de résolution de sélection utilisent cette valeur pour annuler une installation et générer une boîte de dialogue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Présentation de ControlEvent,](controlevent-overview.md)
</dt> <dt>

[**Propriété OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent,](enablerollback-controlevent.md)
</dt> <dt>

[Action CostFinalize](costfinalize-action.md)
</dt> <dt>

[Boîte de dialogue de sélection](selection-dialog.md)
</dt> </dl>

 

 




