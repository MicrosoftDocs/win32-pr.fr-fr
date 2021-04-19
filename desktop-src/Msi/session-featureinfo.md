---
description: La méthode FeatureInfo de l’objet session retourne un objet FeatureInfo qui contient des informations descriptives sur la fonctionnalité spécifiée.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session. FeatureInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532003"
---
# <a name="sessionfeatureinfo-method"></a>Session. FeatureInfo, méthode

La méthode **FeatureInfo** de l’objet [**session**](session-object.md) retourne un objet **FeatureInfo** qui contient des informations descriptives sur la fonctionnalité spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Fonctionnalité* 
</dt> <dd>

Identifie la fonctionnalité qui vous intéresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




