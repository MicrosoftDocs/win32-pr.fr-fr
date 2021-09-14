---
description: 'Si le package d’installation livré avec une application ne se trouve pas à la racine du CD-ROM que les clients reçoivent, la propriété MEDIAPACKAGEPATH doit être définie sur la ligne de commande sur le chemin d’accès relatif de l’application sur le CD-ROM. Par exemple, si le chemin d’accès au package sur le média est E : \\ MyPath \\My.msi, utilisez MEDIAPACKAGEPATH =&\# 0034 ; \\ MyPath \\ & \# 0034 ;. Les administrateurs peuvent créer des CD-ROMs à partir d’un point d’installation d’administration. Si l’emplacement de la racine de l’installation a été modifié sur les nouveaux CD-ROM, la propriété MEDIAPACKAGEPATH doit être définie sur le nouveau chemin d’accès à installer à partir de ce média. Une source avec un emplacement sur le CD-ROM autre que celui spécifié dans le package est inutilisable. Toutefois, il n’est pas nécessaire d’utiliser cette propriété lors de la création d’un point d’installation d’administration à partir de médias d’expédition.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propriété MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021351"
---
# <a name="mediapackagepath-property"></a>Propriété MEDIAPACKAGEPATH

Si le package d’installation livré avec une application ne se trouve pas à la racine du CD-ROM que les clients reçoivent, la propriété **MEDIAPACKAGEPATH** doit être définie sur la ligne de commande sur le chemin d’accès relatif de l’application sur le CD-ROM.

Par exemple, si le chemin d’accès au package sur le média est E : \\ MyPath \\My.msi, utilisez MEDIAPACKAGEPATH = " \\ myPath \\ ".

Les administrateurs peuvent créer des CD-ROMs à partir d’un point d’installation d’administration. Si l’emplacement de la racine de l’installation a été modifié sur les nouveaux CD-ROM, la propriété **MEDIAPACKAGEPATH** doit être définie sur le nouveau chemin d’accès à installer à partir de ce média. Une source avec un emplacement sur le CD-ROM autre que celui spécifié dans le package est inutilisable. Toutefois, il n’est pas nécessaire d’utiliser cette propriété lors de la création d’un point d’installation d’administration à partir de médias d’expédition.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




