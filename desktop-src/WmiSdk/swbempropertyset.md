---
description: Un objet SWbemPropertySet est une collection d’objets SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objet SWbemPropertySet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518069"
---
# <a name="swbempropertyset-object"></a>Objet SWbemPropertySet

Un objet **SWbemPropertySet** est une collection d’objets [**SWbemProperty**](swbemproperty.md) . Vous pouvez ajouter des éléments à la collection à l’aide de la méthode [**Add**](swbempropertyset-add.md) , récupérer des éléments de la collection à l’aide de la méthode [**Item**](swbempropertyset-item.md) et supprimer des éléments de la collection à l’aide de la méthode [**Remove**](swbempropertyset-remove.md) . Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md). Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .

Les objets [**SWbemProperty**](swbemproperty.md) qui composent une collection **SWbemPropertySet** sont utilisés pour décrire les propriétés d’une instance ou d’une classe WMI unique.

## <a name="members"></a>Membres

L’objet **SWbemPropertySet** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemPropertySet** a ces méthodes.



| Méthode                                    | Description                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](swbempropertyset-add.md)       | Ajoute un objet [**SWbemProperty**](swbemproperty.md) à la collection **SWbemPropertySet** .<br/>                        |
| [**Élément**](swbempropertyset-item.md)     | Obtient un [**SWbemProperty**](swbemproperty.md) nommé à partir de la collection. Il s’agit de la méthode par défaut pour cet objet.<br/> |
| [**Remove**](swbempropertyset-remove.md) | Supprime un objet [**SWbemProperty**](swbemproperty.md) de la collection.<br/>                                        |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemPropertySet** a ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Saut**](swbempropertyset-count.md)<br/> | Lecture seule<br/> | Nombre d’éléments dans la collection **SWbemPropertySet** .<br/> |



 

## <a name="examples"></a>Exemples

L’exemple VBScript suivant montre comment [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) peut retourner **wbemErrResetToDefault** si la propriété est substituée.


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




