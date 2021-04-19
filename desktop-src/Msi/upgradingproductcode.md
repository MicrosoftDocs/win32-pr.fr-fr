---
description: La propriété UPGRADINGPRODUCTCODE est définie par Windows Installer lorsqu’une mise à niveau supprime une application.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propriété UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535993"
---
# <a name="upgradingproductcode-property"></a>Propriété UPGRADINGPRODUCTCODE

La propriété **UPGRADINGPRODUCTCODE** est définie par Windows Installer lorsqu’une mise à niveau supprime une application. Le programme d’installation définit cette propriété lors de l’exécution de l' [action RemoveExistingProducts](removeexistingproducts-action.md). Cette propriété n’est pas définie en supprimant une application à l’aide de la commande Ajout/suppression de programmes du panneau de configuration. Une application détermine si elle est supprimée par une mise à niveau ou par l’ajout ou la suppression de programmes en cochant **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




