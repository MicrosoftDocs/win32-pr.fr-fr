---
title: dispinterface (attribut)
description: L’instruction dispinterface définit un ensemble de propriétés et de méthodes sur lesquelles vous pouvez appeler IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- MIDL (MIDL), attribut dispinterface
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842266"
---
# <a name="dispinterface-attribute"></a>dispinterface (attribut)

L’instruction **dispinterface** définit un ensemble de propriétés et de méthodes sur lesquelles vous pouvez appeler **IDispatch :: Invoke**. Une dispinterface peut être définie en répertoriant explicitement l’ensemble des méthodes et des propriétés prises en charge (syntaxe 1), ou en répertoriant une seule interface (syntaxe 2).

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributes* 
</dt> <dd>

Spécifie les attributs qui s’appliquent à l’ensemble de **dispinterface**. Les attributs suivants sont acceptés : **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , non **\[** [**extensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** et **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface-nom* 
</dt> <dd>

Nom par lequel la **dispinterface** est connue dans la bibliothèque de types. Ce nom doit être unique dans la bibliothèque de types.

</dd> <dt>

*liste de propriétés* 
</dt> <dd>

(Syntaxe 1) Liste facultative des propriétés prises en charge par l’objet, déclarées sous la forme de variables. Il s’agit de la forme abrégée de la déclaration des fonctions de propriété dans la liste des méthodes. Pour plus d’informations, consultez la section commentaires.

</dd> <dt>

*List, méthode* 
</dt> <dd>

(Syntaxe 1) Liste comprenant un prototype de fonction pour chaque méthode et propriété de **dispinterface**. Un nombre quelconque de définitions de fonction peuvent apparaître dans *methlist*. Une fonction dans *methlist* se présente sous la forme suivante :

**\[  attributs \]** *ReturnType methname type paramName ***(*** params * * *);**

Les attributs suivants sont acceptés sur une méthode dans une **dispinterface**: **\[ helpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** et **\[** [**vararg**](vararg.md) **\]** . Si **\[ vararg \]** est spécifié, le dernier paramètre doit être un tableau sécurisé de type **Variant** .

La liste de paramètres est une liste délimitée par des virgules, dont chaque élément se présente sous la forme suivante :

**\[***attributs***\]**

Le *type* peut être n’importe quel type déclaré ou intégré, ou un pointeur vers n’importe quel type. Les attributs sur les paramètres sont les suivants :

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**facultatif**](optional.md) **\]** , **\[ String \]**

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

(Syntaxe 2) Nom de l’interface à déclarer en tant qu’interface IDispatch.

</dd> </dl>

## <a name="remarks"></a>Notes

Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :

1.  Paramètres obligatoires (paramètres qui n’ont pas les \[ \] attributs DefaultValue ou \[ facultatifs \] )
2.  paramètres facultatifs avec ou sans \[ l' \] attribut DefaultValue,
3.  paramètres avec l' \[ \] attribut facultatif et sans l' \[ \] attribut DefaultValue,
4.  \[paramètre [**LCID**](lcid.md) \] , le cas échéant,
5.  \[[**retVal**](retval.md) \] paramètre

Les fonctions de méthode sont spécifiées exactement comme décrit dans la page de référence du [**module**](module.md) , sauf que l’attribut d' \[ [**entrée**](entry.md) \] n’est pas autorisé. Notez que STDOLE32. TLB (STDOLE. TLB sur les systèmes 16 bits) doit être importé, car une **dispinterface** hérite de IDispatch.

Vous pouvez déclarer des propriétés dans les listes de propriétés ou de méthodes. La déclaration de propriétés dans la liste Propriétés n’indique pas le type d’accès pris en charge par la propriété (c’est-à-dire, l’extraction, la mise en place ou la PutRef). Spécifiez l' \[ [](readonly.md) \] attribut ReadOnly pour les propriétés qui ne prennent pas en charge put ou PutRef. Si vous déclarez les fonctions de propriété dans la liste des méthodes, les fonctions d’une propriété ont toutes le même identificateur.

À l’aide de la première syntaxe, les balises Properties : et Methods sont requises. L' \[ attribut [**ID**](id.md) \] est également requis sur chaque membre. Par exemple :

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

Contrairement aux membres d’interface, les membres dispinterface ne peuvent pas utiliser l’attribut [**retVal**](retval.md) pour retourner une valeur en plus d’un code d’erreur HRESULT. L' \[ [](lcid.md) \] attribut LCID est également non valide pour les dispinterfaces, car IDispatch :: Invoke passe un LCID. Toutefois, il est possible de redéclarer une interface qui utilise ces attributs.

À l’aide de la deuxième syntaxe, les interfaces qui prennent en charge IDispatch et sont déclarées précédemment dans un script ODL peuvent être redéclarées comme des interfaces IDispatch comme suit :

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

L’exemple précédent déclare tous les membres de Hello et tous les membres que Hello hérite de en prenant en charge IDispatch. Dans ce cas, si Hello a été déclaré précédemment avec des \[ \] membres LCID et \[ retval \] qui retournaient HRESULT, mktyplib supprimerait chaque \[ \] paramètre LCID et le type de retour HRESULT, et marquera à la place le type de retour comme celui du \[ \] paramètre retval.

> [!Note]  
> L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.

 

Les propriétés et les méthodes d’une dispinterface ne font pas partie du VTBL de la dispinterface. Par conséquent, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) et [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) ne peuvent pas être utilisés pour implémenter IDispatch :: Invoke. La dispinterface est utilisée lorsqu’une application doit exposer des fonctions non VTBL existantes par le biais de l’automatisation. Ces applications peuvent implémenter IDispatch :: Invoke en examinant le paramètre dispidMember et en appelant directement la fonction correspondante.

## <a name="examples"></a>Exemples

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**masquer**](hidden.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**facultatif**](optional.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**sensible**](restricted.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 