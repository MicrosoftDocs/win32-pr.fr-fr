---
description: Retourne un objet RecordList qui énumère la liste des produits.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Installer. ProductsEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9320ef38fefd32c60b7022923add5ca55d609d82ff01b8654104bb35b1dbf6be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074929"
---
# <a name="installerproductsex-property"></a>Installer. ProductsEx, propriété

La propriété **ProductsEx** retourne un objet [**RecordList**](recordlist-object.md) qui énumère la liste des produits. Cette propriété appelle [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Programme d’installation**](installer-object.md)
</dt> <dt>

[**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Produit**](product-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




