---
description: La propriété FeatureState en lecture seule retourne l’état installé d’une fonctionnalité.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer. FeatureState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989abe860848b943e77b02910e9760f8fcaecc97fd8a2634f8147605577613d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631273"
---
# <a name="installerfeaturestate-property"></a>Installer. FeatureState, propriété

La propriété **FeatureState** en lecture seule retourne l’état installé d’une fonctionnalité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Cette propriété retourne l’une des valeurs suivantes.



| Valeur                     | Description                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | La fonctionnalité n’est pas installée.                    |
| msiInstallStateAdvertised | La fonctionnalité est publiée.                       |
| msiInstallStateLocal      | La fonctionnalité est installée pour s’exécuter localement.         |
| msiInstallStateSource     | La fonctionnalité est installée pour s’exécuter à partir de la source.     |
| msiInstallStateInvalidArg | Un paramètre non valide a été passé à la fonction. |
| msiInstallStateUnknown    | Le code du produit ou l’ID de fonctionnalité est inconnu.       |
| msiInstallStateBadConfig  | Les données de configuration sont endommagées.               |



 

 

La propriété **FeatureState** ne valide pas le fait que la fonctionnalité soit accessible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




