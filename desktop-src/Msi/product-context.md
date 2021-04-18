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
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526774"
---
# <a name="productcontext-property"></a>Propriété Product. Context

La propriété de **contexte** retourne le contexte de ce produit.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Cette propriété peut retourner l’une des valeurs suivantes.



| Context                        | Valeur | Signification                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Produits sous un contexte géré.   |
| \_utilisateur MSIINSTALLCONTEXT        | 2     | Produits sous un contexte non managé. |
| \_machine MSIINSTALLCONTEXT     | 4     | Produits sous le contexte de l’ordinateur.   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Production**](product-object.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




