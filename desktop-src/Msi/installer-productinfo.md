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
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745289"
---
# <a name="installerproductinfo-property"></a>Installer. ProductInfo, propriété

La propriété **ProductInfo** est une propriété en lecture seule qui retourne la valeur de l’attribut spécifié pour un produit installé ou publié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

La propriété **ProductInfo** (« LocalPackage ») ne retourne pas nécessairement un chemin d’accès au package mis en cache. Les installations en mode maintenance ne doivent pas être appelées à partir du LocalPackage. Le package mis en cache est réservé aux utilisations internes.

## <a name="requirements"></a>Configuration requise



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

 

 




