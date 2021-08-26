---
description: La propriété de contexte retourne le contexte de ce produit.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Propriété Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21fb23a595b1f479f2468f0006cca7cd9218de03fc2cc76b794caae79ea45a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129119"
---
# <a name="productcontext-property"></a>Propriété Product. Context

La propriété de **contexte** retourne le contexte de ce produit.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Cette propriété peut retourner l’une des valeurs suivantes.



| Contexte                        | Valeur | Signification                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Produits sous un contexte géré.   |
| \_utilisateur MSIINSTALLCONTEXT        | 2     | Produits sous un contexte non managé. |
| \_machine MSIINSTALLCONTEXT     | 4     | Produits sous le contexte de l’ordinateur.   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Production**](product-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




