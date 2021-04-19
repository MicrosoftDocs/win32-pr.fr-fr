---
description: La propriété FeatureValidStates de l’objet session retourne un entier représentant des indicateurs binaires avec chaque bit approprié représentant un état d’installation valide pour la fonctionnalité spécifiée.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session. FeatureValidStates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521651"
---
# <a name="sessionfeaturevalidstates-property"></a>Session. FeatureValidStates, propriété

La propriété **FeatureValidStates** de l’objet [**session**](session-object.md) retourne un entier représentant des indicateurs binaires avec chaque bit approprié représentant un état d’installation valide pour la fonctionnalité spécifiée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valeur de la propriété

Nom de chaîne requis de l’élément de fonctionnalité dont les États d’installation valides doivent être récupérés.

## <a name="remarks"></a>Notes

La valeur de retour est composée d’indicateurs binaires, comme suit. Bit 0 : s’il est défini, local est un état valide. Bit 1 : s’il est défini, la source est un état valide.

La propriété **FeatureValidStates** ne fonctionne que si le programme d’installation a appelé les actions [CostInitialize](costinitialize-action.md) et [CostFinalize](costfinalize-action.md) .

**FeatureValidStates** détermine la validité de l’État en interrogeant tous les composants liés à la fonctionnalité spécifiée sans tenir compte de l’état d’installation actuel d’un composant.

Les États valides possibles pour une fonctionnalité sont déterminés comme suit :

-   Si la fonctionnalité ne contient pas de composants, les deux versions \_ \_ de la source de l’élément InstallState locale et de la source InstallState sont valides pour la fonctionnalité.
-   Si au moins un composant de la fonctionnalité a un attribut msidbComponentAttributesLocalOnly ou msidbComponentAttributesOptional, INSTALLSTATE \_ local est un état valide pour la fonctionnalité.
-   Si au moins un composant de la fonctionnalité a un attribut msidbComponentAttributesSourceOnly ou msidbComponentAttributesOptional, INSTALLSTATE \_ source est un état valide pour la fonctionnalité.
-   Si un fichier d’un composant appartenant à la fonctionnalité est corrigé ou provient d’une source compressée, \_ la source INSTALLSTATE n’est pas incluse dans un état valide pour la fonctionnalité.
-   INSTALLSTATE \_ advertise n’est pas un état valide si la fonctionnalité interdit la publication (msidbFeatureAttributesDisallowAdvertise) ou si la fonctionnalité requiert la prise en charge de la plateforme pour la publication (msidbFeatureAttributesNoUnsupportedAdvertise) et que la plateforme ne la prend pas en charge.
-   INSTALLSTATE \_ absent est un état valide pour la fonctionnalité si ses attributs n’incluent pas msidbFeatureAttributesUIDisallowAbsent.
-   Les États valides pour les fonctionnalités enfants marquées pour suivre la fonctionnalité parente (msidbFeatureAttributesFollowParent) sont basés sur l’action de la fonctionnalité parente ou sur l’état installé.

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




