---
description: La propriété FeatureUsageDate est une propriété en lecture seule qui retourne la date de la dernière utilisation de la fonctionnalité spécifiée.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer. FeatureUsageDate, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121605"
---
# <a name="installerfeatureusagedate-property"></a>Installer. FeatureUsageDate, propriété

La propriété **FeatureUsageDate** est une propriété en lecture seule qui retourne la date de la dernière utilisation de la fonctionnalité spécifiée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

L’utilisation des méthodes [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou de leurs équivalents d’API sur la fonctionnalité spécifiée définit cette propriété.

La date est au format de date MS-DOS, comme indiqué dans le tableau suivant.



| Bits | Contenu                                            |
|------|-----------------------------------------------------|
| 0-4  | Jour du mois (1-31)                             |
| 5-8  | Month (1 = janvier, 2 = février, etc.)        |
| 9-15 | Décalage d’année à partir de 1980 (Ajouter 1980 pour atteindre l’année réelle) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




