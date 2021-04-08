---
title: defaultvtable (attribut)
description: L’attribut \ defaultvtable \ définit une interface en tant qu’interface vtable par défaut.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- MIDL de l’attribut defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842233"
---
# <a name="defaultvtable-attribute"></a>defaultvtable (attribut)

L’attribut **\[ defaultvtable \]** définit une interface en tant qu’interface vtable par défaut.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*coclass-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la classe. Les **\[** [](source.md) **\]** attributs source et **\[** [**UUID**](uuid.md) **\]** sont requis.

</dd> <dt>

*nom de la coclasse* 
</dt> <dd>

Nom de la classe.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Liste des interfaces pour la classe.

</dd> </dl>

## <a name="remarks"></a>Notes

Une interface vtable par défaut ne peut pas être une dispinterface ; il doit s’agir d’une interface double ou vtable ou d’une interface. Si l’interface est une interface double, les récepteurs peuvent supposer qu’ils recevront des événements via vtable.

Une classe peut être à la fois une interface source par défaut et une interface source vtable par défaut, comme indiqué dans l’exemple. Dans ce cas, un récepteur de notification doit utiliser \_ l’IID IDISPATCH pour recevoir les événements de dispatch et utiliser l’identificateur d’interface pour recevoir des événements vtable.

### <a name="typeflag-representation"></a>Représentation TYPEFLAG

Présence de IMPLTYPEFLAG \_ FDEFAULTVTABLE.

## <a name="examples"></a>Exemples

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**code**](source.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> </dl>

 

 