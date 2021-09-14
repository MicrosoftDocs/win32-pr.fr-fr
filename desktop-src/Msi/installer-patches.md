---
description: La propriété patchs en lecture seule de l’objet installer retourne un objet StringList qui contient tous les correctifs appliqués au produit.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer. patches, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012131"
---
# <a name="installerpatches-property"></a>Installer. patches, propriété

La propriété **patchs** en lecture seule de l’objet [**installer**](installer-object.md) retourne un objet [**StringList**](stringlist-object.md) qui contient tous les correctifs appliqués au produit.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le code du produit.

## <a name="remarks"></a>Notes

Pour énumérer les correctifs, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les correctifs ne sont pas triés, les nouveaux correctifs ont un index arbitraire. Cela signifie que la fonction peut retourner des correctifs dans n’importe quel ordre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




