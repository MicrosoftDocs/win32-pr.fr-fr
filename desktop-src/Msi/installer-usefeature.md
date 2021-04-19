---
description: La méthode UseFeature de l’objet installer incrémente le nombre d’utilisations d’une fonctionnalité particulière et retourne l’état d’installation de cette fonctionnalité. Cette méthode doit être utilisée pour indiquer l’intention d’une application d’utiliser une fonctionnalité.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. UseFeature, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535359"
---
# <a name="installerusefeature-method"></a>Installer. UseFeature, méthode

La méthode **UseFeature** de l’objet [**installer**](installer-object.md) incrémente le nombre d’utilisations d’une fonctionnalité particulière et retourne l’état d’installation de cette fonctionnalité. Cette méthode doit être utilisée pour indiquer l’intention d’une application d’utiliser une fonctionnalité.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code de produit du produit.

</dd> <dt>

*Fonctionnalité* 
</dt> <dd>

Identifie la fonctionnalité à utiliser.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Ce paramètre doit être *msiInstallModeNoDetection*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **UseFeature** doit uniquement être utilisée sur les fonctionnalités dont la publication est connue. L’application doit déterminer l’état de la fonctionnalité en appelant la propriété [**FeatureState**](installer-featurestate.md) ou la propriété [**features**](installer-features.md) ou leurs équivalents d’API.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




