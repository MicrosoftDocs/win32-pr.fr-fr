---
description: La propriété Qualifiers \_ de l’objet SWbemObject retourne un objet SWbemQualifierSet qui est une collection des qualificateurs de l’instance ou de la classe actuelle. Cette propriété est en lecture seule.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732489"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject. Qualifiers, \_ propriété

La propriété **Qualifiers \_** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemQualifierSet**](swbemqualifierset.md) qui est une collection des qualificateurs de l’instance ou de la classe actuelle. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

La [liste de tous les qualificateurs d’un exemple de](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) code VBScript de classe WMI dans la Galerie TechNet utilise la \_ propriété qualifier pour répertorier les qualificateurs de classe pour une classe WMI spécifiée.

La [liste de toutes les classes abstraites dans](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) l’exemple de code WMI VBScript sur la Galerie TechNet répertorie toutes les classes WMI abstraites définies dans l' \\ espace de noms CIMV2 racine.

L’exemple de code [List All Dynamic classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript utilise la \_ propriété qualifier pour répertorier toutes les classes dynamiques WMI (y compris les classes d’association) définies dans l' \\ espace de noms CIMV2 racine.

L’exemple de code [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell sur la Galerie TechNet répertorie toutes les propriétés accessibles en écriture dans l’espace de noms spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




