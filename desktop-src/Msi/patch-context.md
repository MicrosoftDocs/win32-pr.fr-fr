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
ms.openlocfilehash: 3316c71c5de15a777ce7e4559b7ee52e9efcb61200bd72b8898440e56bb4f392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042419"
---
# <a name="patchcontext-property"></a>Patch. Context, propriété

La propriété **Context** retourne le contexte de ce correctif.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Cette propriété retourne l’une des valeurs suivantes.



| Contexte                        | Valeur | Signification                        |
|--------------------------------|-------|--------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Correctif sous le contexte géré.   |
| \_utilisateur MSIINSTALLCONTEXT        | 2     | Correctif sous un contexte non managé. |
| \_machine MSIINSTALLCONTEXT     | 4     | Correctif sous le contexte de l’ordinateur.   |



 

## <a name="requirements"></a>Configuration requise



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

 

 




