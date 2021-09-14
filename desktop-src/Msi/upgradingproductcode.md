---
description: la propriété UPGRADINGPRODUCTCODE est définie par Windows Installer lorsqu’une mise à niveau supprime une application.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propriété UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021238"
---
# <a name="upgradingproductcode-property"></a>Propriété UPGRADINGPRODUCTCODE

la propriété **UPGRADINGPRODUCTCODE** est définie par Windows Installer lorsqu’une mise à niveau supprime une application. Le programme d’installation définit cette propriété lors de l’exécution de l' [action RemoveExistingProducts](removeexistingproducts-action.md). Cette propriété n’est pas définie en supprimant une application à l’aide de la commande Ajout/suppression de programmes du panneau de configuration. Une application détermine si elle est supprimée par une mise à niveau ou par l’ajout ou la suppression de programmes en cochant **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




