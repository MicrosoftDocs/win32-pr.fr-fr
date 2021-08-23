---
description: Le programme d’installation définit la valeur de la propriété MsiRestartManagerSessionKey sur la clé de session pour la session du gestionnaire de redémarrage.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propriété MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f48fe8d2ce4b287afc5c222acdc1f71eec393ff9a1ab1773a822e30405e6a317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944537"
---
# <a name="msirestartmanagersessionkey-property"></a>Propriété MsiRestartManagerSessionKey

Le programme d’installation définit la valeur de la propriété **MsiRestartManagerSessionKey** sur la clé de session pour la session du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) . Les actions personnalisées peuvent utiliser la clé de session pour rejoindre la session du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) .

## <a name="remarks"></a>Remarques

Le programme d’installation définit la valeur de la propriété **MsiRestartManagerSessionKey** lors de l’initialisation, puis efface la valeur lors de l’action [InstallValidate](installvalidate-action.md) . Les actions personnalisées qui ont besoin de la valeur de la propriété **MsiRestartManagerSessionKey** doivent être prévenues de l’action InstallValidate dans la séquence d’action.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
