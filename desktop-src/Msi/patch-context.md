---
description: La propriété Context retourne le contexte de ce correctif.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch. Context, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218769"
---
# <a name="patchcontext-property"></a>Patch. Context, propriété

La propriété **Context** retourne le contexte de ce correctif.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Cette propriété retourne l’une des valeurs suivantes.



| Context                        | Valeur | Signification                        |
|--------------------------------|-------|--------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Correctif sous le contexte géré.   |
| \_utilisateur MSIINSTALLCONTEXT        | 2     | Correctif sous un contexte non managé. |
| \_machine MSIINSTALLCONTEXT     | 4     | Correctif sous le contexte de l’ordinateur.   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet patch**](patch-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




