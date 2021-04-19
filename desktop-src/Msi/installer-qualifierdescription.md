---
description: La propriété QualifierDescription en lecture seule retourne une chaîne de texte décrivant le composant qualifié.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer. QualifierDescription, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530351"
---
# <a name="installerqualifierdescription-property"></a>Installer. QualifierDescription, propriété

La propriété **QualifierDescription** en lecture seule retourne une chaîne de texte décrivant le composant qualifié. Cette chaîne localisable est créée dans la colonne AppData de la [table PublishComponent](publishcomponent-table.md) et peut être affichée à l’utilisateur. Le qualificateur fait la distinction entre plusieurs formes du même composant, par exemple un composant implémenté dans plusieurs langues.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Composants qualifiés](qualified-components.md)
</dt> </dl>

 

 




