---
description: L’objet patch représente une instance unique d’un correctif qui a été inscrit ou appliqué. L’objet peut être instancié avec la propriété patch comme &\# 0034 ; WindowsInstaller. installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034 ;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Objet patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9e337af735a39312cb5aa740283cb8b4d8b508be33f28c302788a1207f89472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074839"
---
# <a name="patch-object"></a>Objet patch

L’objet **patch** représente une instance unique d’un correctif qui a été inscrit ou appliqué.

L’objet peut être instancié avec la propriété **patch** comme « windowsinstaller. installer. patch (*PatchCode*, *ProductCode*, *UserSid*, *Context*) ». Pour un contexte d’ordinateur, le paramètre *UserSid* doit être une chaîne vide. La valeur *ProductCode* peut être définie sur une chaîne vide pour les correctifs qui sont inscrits uniquement et qui ne sont pas encore appliqués à un produit. La valeur *ProductCode* peut être définie sur une chaîne vide lors de la lecture ou de la mise à jour des informations de liste source d’un correctif.

## <a name="members"></a>Membres

L’objet **patch** a les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **patch** a ces méthodes.



| Méthode                                                               | Description                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Ajoutez un disque à l’ensemble de disques inscrits.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Ajoutez une source réseau ou URL à la liste source. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Efface la liste source complète du type spécifié de sources.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Supprimer un disque de l’ensemble de disques inscrits de la liste source. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Supprimer une source de réseau ou d’URL de la liste source.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Efface la dernière source utilisée de la liste source. Cela force une résolution de liste source la prochaine fois que la source est requise.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **patch** a ces propriétés.



| Propriété                                                  | Description                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Contexte**](patch-context.md)<br/>               | Le contexte de cette instance de patch est une valeur MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Énumère tous les disques multimédias pour cette instance de correctif.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Retourne le code du correctif.<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | Obtient des informations de propriété sur un correctif spécifique appliqué à une instance spécifique du produit.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Retourne le code du produit.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Obtient et définit les propriétés des informations sur la source. Il s’agit d’une propriété de lecture ou d’écriture.<br/>              |
| [**Sources**](patch-sources.md)<br/>               | Énumère toutes les sources pour cette instance du correctif.<br/>                                             |
| [**Département**](patch-state.md)<br/>                   | État d’installation du correctif.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Retourne le SID de l’utilisateur, sous le compte pour lequel cette instance de correctif est disponible.<br/>                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




