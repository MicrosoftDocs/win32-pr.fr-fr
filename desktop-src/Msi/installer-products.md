---
description: La propriété Products est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Installer. Products, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bd93b21b01721be8d4be0e432f83c507762b5d76c758419ed157c85f8a0ac419
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388139"
---
# <a name="installerproducts-property"></a>Installer. Products, propriété

La propriété **Products** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Pour énumérer les produits, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each. Étant donné que les produits ne sont pas triés, tous les nouveaux produits possèdent un index arbitraire. Cela signifie que la fonction peut retourner des produits dans n’importe quel ordre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




