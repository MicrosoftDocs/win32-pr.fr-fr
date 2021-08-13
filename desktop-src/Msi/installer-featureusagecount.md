---
description: La propriété FeatureUsageCount est une propriété en lecture seule qui retourne le nombre de fois que la fonctionnalité a été utilisée.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Installer. FeatureUsageCount, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f0f8444909d07655949cd35d060eb455e5a153fc2b897e757c2fdde2d1d731d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631198"
---
# <a name="installerfeatureusagecount-property"></a>Installer. FeatureUsageCount, propriété

La propriété **FeatureUsageCount** est une propriété en lecture seule qui retourne le nombre de fois que la fonctionnalité a été utilisée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

L’utilisation des méthodes [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou de leurs équivalents d’API sur la fonctionnalité spécifiée incrémente cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




