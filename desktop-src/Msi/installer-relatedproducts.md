---
description: La propriété RelatedProducts en lecture seule retourne un objet StringList énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels avec une propriété UpgradeCode spécifiée dans leur table de propriétés.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer. RelatedProducts, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012093"
---
# <a name="installerrelatedproducts-property"></a>Installer. RelatedProducts, propriété

La propriété **RelatedProducts** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels avec une propriété [**UpgradeCode**](upgradecode.md) spécifiée dans leur table de [Propriétés](property-table.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valeur de la propriété

Code de mise à niveau des produits connexes que le programme d’installation énumère.

## <a name="remarks"></a>Notes

Pour énumérer les produits connexes, une application itère au sein du [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les produits associés ne sont pas triés, tous les nouveaux produits associés possèdent un index arbitraire. Cela signifie que la fonction peut retourner des produits connexes dans n’importe quel ordre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




