---
description: La propriété State retourne l’état d’installation de cette instance du correctif.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Propriété patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b28eee03cfc74537c8be7669124a4f70db40ca88196678889553978232c934c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942289"
---
# <a name="patchstate-property"></a>Propriété patch. State

La propriété **State** retourne l’état d’installation de cette instance du correctif.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Cette propriété retourne l’une des valeurs suivantes.



| État de l’installation        | Signification                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ appliqué    | Le correctif est appliqué à cette instance de produit.                   |
| MSIPATCHSTATE \_ remplacé | Le correctif est appliqué à cette instance de produit, mais il est remplacé. |
| MSIPATCHSTATE \_ obsolète  | Le correctif est appliqué dans cette instance du produit, mais il est obsolète.      |



 

Cette méthode peut retourner \_ une erreur Unknown \_ patch, si l’objet [**patch**](patch-object.md) est initialisé avec une chaîne vide pour *ProductCode*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




