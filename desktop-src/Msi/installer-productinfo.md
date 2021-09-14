---
description: La propriété ProductInfo est une propriété en lecture seule qui retourne la valeur de l’attribut spécifié pour un produit installé ou publié.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Installer. ProductInfo, propriété (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012118"
---
# <a name="installerproductinfo-property"></a>Installer. ProductInfo, propriété

La propriété **ProductInfo** est une propriété en lecture seule qui retourne la valeur de l’attribut spécifié pour un produit installé ou publié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

La propriété **ProductInfo** (« LocalPackage ») ne retourne pas nécessairement un chemin d’accès au package mis en cache. Les installations en mode maintenance ne doivent pas être appelées à partir du LocalPackage. Le package mis en cache est réservé aux utilisations internes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| En-tête<br/>  | <dl> <dt>Oemupgex. h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




