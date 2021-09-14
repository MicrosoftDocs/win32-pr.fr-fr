---
description: L’objet SWbemProperty représente une propriété WMI unique d’un objet managé. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objet SWbemProperty (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010420"
---
# <a name="swbemproperty-object"></a>Objet SWbemProperty

L’objet **SWbemProperty** représente une propriété WMI unique d’un objet managé. Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membres

L’objet **SWbemProperty** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SWbemProperty** a ces propriétés.



| Propriété                                                     | Type d’accès           | Description                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | Lecture seule<br/>  | Type de cette propriété.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Lecture seule<br/>  | Valeur booléenne qui indique si cette propriété a un type de tableau.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Lecture seule<br/>  | Valeur booléenne qui indique si cette propriété est locale.<br/>                                                            |
| [**Nomme**](swbemproperty-name.md)<br/>                | Lecture seule<br/>  | Nom de cette propriété WMI.<br/>                                                                                         |
| [**Origine**](swbemproperty-origin.md)<br/>            | Lecture seule<br/>  | Contient la classe d’origine de cette propriété.<br/>                                                                   |
| [**Qualificateurs\_**](swbemproperty-qualifiers-.md)<br/> | Lecture seule<br/>  | Objet [**SWbemQualifierSet**](swbemqualifierset.md) , qui est la collection de qualificateurs pour cette propriété.<br/> |
| [**Ajoutée**](swbemproperty-value.md)<br/>              | Lecture/écriture<br/> | Valeur réelle de cette propriété. Il s’agit de la propriété Automation par défaut de cet objet.<br/>                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




