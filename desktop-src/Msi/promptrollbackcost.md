---
description: La propriété PROMPTROLLBACKCOST spécifie l’action effectuée par le programme d’installation si les fonctionnalités d’annulation de la restauration sont activées et que l’espace disque est insuffisant pour terminer l’installation. Les valeurs possibles de PROMPTROLLBACKCOST sont les suivantes. ValueActionPDisplay boîte de dialogue qui vous demande s’il faut continuer sans restauration. DDisable Rollback et continue sans demander à l’utilisateur. FFail avec l’invite d’erreur d’espace disque insuffisant.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propriété PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71cca3134593039354735e2e306a924620db8100eb0fd0e0a51f392c58f61897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129039"
---
# <a name="promptrollbackcost-property"></a>Propriété PROMPTROLLBACKCOST

La propriété **PROMPTROLLBACKCOST** spécifie l’action effectuée par le programme d’installation si les fonctionnalités d’annulation de la [restauration](rollback-installation.md) sont activées et que l’espace disque est insuffisant pour terminer l’installation.

Les valeurs possibles de **PROMPTROLLBACKCOST** sont les suivantes.



| Valeur | Action                                                              |
|-------|---------------------------------------------------------------------|
| P     | Affiche une boîte de dialogue qui vous demande s’il faut continuer sans restauration. |
| D     | Désactivez la restauration et continuez sans demander à l’utilisateur.                  |
| F     | Échoue avec l’invite d’erreur d’espace disque insuffisant.                       |



 

## <a name="remarks"></a>Remarques

Lorsque l’interface utilisateur est exécutée au niveau de base ou pas de l’interface utilisateur, le programme d’installation gère automatiquement la logique d’espace disque insuffisant.

Lorsque l’interface utilisateur s’exécute au niveau complet, des options supplémentaires peuvent être fournies à l’utilisateur, telles que l’invite avant de procéder à une restauration, la désactivation de la restauration ou la poursuite sans restauration lorsque le disque est plein. Il revient au développeur du package de créer la séquence de la boîte de dialogue pour fournir les choix appropriés à l’utilisateur. Les éléments disponibles sont les [EnableRollback ControlEvent,](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) Property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) Property et **PROMPTROLLBACKCOST** Property.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




