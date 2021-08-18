---
description: La propriété ProductState est une propriété en lecture seule qui retourne les informations d’état d’installation d’un produit.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Méthode de propriété installer. ProductState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c19a712c4838905296026a2a0bea4c9e1abc1c49465a854692dd603734e0bd89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763619"
---
# <a name="installerproductstate-property-method"></a>Méthode de propriété installer. ProductState

La **propriété ProductState** est une propriété en lecture seule qui retourne les informations d’état d’installation d’un produit.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code de produit du produit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Retourne l’une des valeurs indiquées dans le tableau suivant.



| État de l'installation        | Description                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | Le produit est installé pour un autre utilisateur.   |
| msiInstallStateDefault    | Le produit est installé pour l’utilisateur actuel.   |
| msiInstallStateAdvertised | Le produit est publié, mais n’est pas installé.     |
| msiInstallStateInvalidArg | Un paramètre non valide a été passé à la fonction. |
| msiInstallStateUnknown    | Le produit n’est ni publié ni installé. |
| msiInstallStateBadConfig  | Les données de configuration sont endommagées.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




