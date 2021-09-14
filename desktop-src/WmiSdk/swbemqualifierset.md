---
description: Un objet SWbemQualifierSet est une collection d’objets SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objet SWbemQualifierSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010388"
---
# <a name="swbemqualifierset-object"></a>Objet SWbemQualifierSet

Un objet **SWbemQualifierSet** est une collection d’objets [**SWbemQualifier**](swbemqualifier.md) . Les éléments sont ajoutés à la collection à l’aide de la méthode [**Add**](swbemqualifierset-add.md) , récupérés à partir de la collection à l’aide de la méthode [**Item**](swbemqualifierset-item.md) et supprimés de la collection à l’aide de la méthode [**Remove**](swbemqualifierset-remove.md) . Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .

Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

Les objets [**SWbemQualifier**](swbemqualifier.md) qui composent une collection **SWbemQualifierSet** décrivent les qualificateurs attachés à une classe, une instance, une méthode ou un paramètre de méthode WMI.

## <a name="members"></a>Membres

L’objet **SWbemQualifierSet** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemQualifierSet** a ces méthodes.



| Méthode                                     | Description                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](swbemqualifierset-add.md)       | Ajoute un objet [**SWbemQualifier**](swbemqualifier.md) à la collection **SWbemQualifierSet** .<br/> |
| [**Élément**](swbemqualifierset-item.md)     | Retourne un objet nommé [**SWbemQualifier**](swbemqualifier.md) à partir de la collection.<br/>             |
| [**Supprimer**](swbemqualifierset-remove.md) | Supprime un qualificateur nommé de la collection.<br/>                                                   |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemQualifierSet** a ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Count**](swbemqualifierset-count.md)<br/> | Lecture seule<br/> | Contient le nombre d’éléments d’une collection **SWbemQualifierSet** .<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




