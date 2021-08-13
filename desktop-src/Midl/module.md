---
title: attribut de module
description: L’instruction module définit un groupe de fonctions, en général un ensemble de points d’entrée de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- attribut de module MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642807"
---
# <a name="module-attribute"></a>attribut de module

L’instruction **module** définit un groupe de fonctions, en général un ensemble de points d’entrée de dll.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributes* 
</dt> <dd>

Les \[ attributs [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] et \[ [**DllName**](dllname-str-.md) \] sont acceptés avant une instruction **module** . Pour plus d’informations sur les attributs acceptés avant une définition de module, consultez [descriptions d’attributs](/previous-versions/windows/desktop/automat/attribute-descriptions)dans le livre OLE Automation. L' \[ attribut **DllName** \] est obligatoire. Si l' \[  \] attribut UUID est omis, le module n’est pas spécifié de manière unique dans le système.

</dd> <dt>

*NomModule* 
</dt> <dd>

Nom du module.

</dd> <dt>

*elementlist* 
</dt> <dd>

Liste des définitions de constantes et des prototypes de fonction pour chaque fonction dans la DLL. Un nombre quelconque de définitions de fonction peuvent apparaître dans la liste de fonctions. Une fonction dans la liste de fonctions se présente sous la forme suivante :

\[*attributs* \] *ReturnType* \[ *Convention d’appel funcname* \] (*params*);

\[*attributs* \] [**const**](const.md) constantType *constname*  =  *constval*;

Seuls les \[ [](helpstring.md) \] attributs HelpString et \[ [**HelpContext**](helpcontext.md) \] sont acceptés pour une [**constante const**](const.md).

Les attributs suivants sont acceptés sur une fonction d’un module : \[ [**helpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] et \[ [**vararg**](vararg.md) \] . Si \[ **vararg** \] est spécifié, le dernier paramètre doit être un tableau sécurisé de type **Variant** .

La Convention d’appel facultative peut être \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl, ou \_ \_ StdCall/ \_ StdCall/StdCall. Le *type de convention d’appel paramName* peut inclure jusqu’à deux traits de soulignement de début.

La liste de paramètres est une liste délimitée par des virgules de :

\[*attributs*\]

Le type peut être n’importe quel type précédemment déclaré ou type intégré, un pointeur vers tout type ou un pointeur vers un type intégré. Les attributs sur les paramètres sont les suivants :

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**facultatif**](optional.md) \] .

Si \[ [](optional.md) \] cette option est utilisée, les types de ces paramètres doivent être **Variant** ou **Variant** \* .

</dd> </dl>

## <a name="remarks"></a>Remarques

La sortie du fichier d’en-tête (. h) pour les modules est une série de prototypes de fonction. Le mot clé **module** et les crochets environnants sont supprimés de la sortie du fichier d’en-tête (. h), mais un commentaire (// *modulename* du **module** ) est inséré avant les prototypes. Le mot clé **extern** est inséré avant les déclarations.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Contenu d’une bibliothèque de types](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**DllName**](dllname-str-.md)
</dt> <dt>

[**mention**](entry.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**masquer**](hidden.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**universel**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 