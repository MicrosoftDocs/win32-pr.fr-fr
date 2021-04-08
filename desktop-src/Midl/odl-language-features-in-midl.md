---
title: Fonctionnalités du langage ODL dans MIDL
description: Attributs ODL (Object Description Language), Mots clés, instructions et directives qui font partie de MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL et ODL MIDL, fonctionnalités de langage
- ODL MIDL, en MIDL
- ODL MIDL, attributs
- ODL MIDL, Mots clés
- ODL MIDL, instructions
- ODL MIDL, directives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840614"
---
# <a name="odl-language-features-in-midl"></a>Fonctionnalités du langage ODL dans MIDL

> [!Note]  
> L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.

 

Les rubriques suivantes répertorient les attributs ODL (Object Description Language), les mots clés, les instructions et les directives qui font désormais partie du Microsoft Interface Definition Language (MIDL) :

-   [Attributs ODL](#odl-attributes)
-   [Mots clés, instructions et directives ODL](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a>Attributs ODL



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| \[[**appobject**](appobject.md)\]         | \[[**pouvant être liée**](bindable.md)\]       |
| \[[**régulation**](control.md)\]             | \[[**valeurs**](default.md)\]         |
| \[[**DefaultValue**](defaultvalue.md)\]   | \[[**displaybind**](displaybind.md)\] |
| \[[**DllName**](dllname-str-.md)\]        | \[[**double**](dual.md)\]               |
| \[[**mention**](entry.md)\]                 | \[[**HelpContext**](helpcontext.md)\] |
| \[[**HelpString**](helpstring.md)\]       | \[[**HelpFile**](helpfile.md)\]       |
| \[[**masquer**](hidden.md)\]               | \[[**identifi**](id.md)\]                   |
| \[[**immediatebind**](immediatebind.md)\] | \[[**dans**](in.md)\]                   |
| \[[**LCID**](lcid.md)\]                   | \[[**accordée**](licensed.md)\]       |
| \[[**PerformanceCategory**](nonextensible.md)\] | \[[**ODL**](odl.md)\]                 |
| \[[**oleautomation**](oleautomation.md)\] | \[[**facultatif**](optional.md)\]       |
| \[[**à**](out-idl.md)\]                 | \[[**propget**](propget.md)\]         |
| \[[**propput**](propput.md)\]             | \[[**propputref**](propputref.md)\]   |
| \[[**publique**](public.md)\]               | \[[ **lecture seule**](readonly.md)\]      |
| \[[**modification**](requestedit.md)\]     | \[[**sensible**](restricted.md)\]   |
| \[[**retval**](retval.md)\]               | \[[**code**](source.md)\]           |
| \[[**universel**](uuid.md)\]                   | [**vararg**](vararg.md)\]             |
| \[[**Version**](version.md)\]             | Â                                      |



 

## <a name="odl-keywords-statements-and-directives"></a>Mots clés, instructions et directives ODL



|                                        |
|----------------------------------------|
| [**coclasse**](coclass.md)             |
| [**dispinterface**](dispinterface.md) |
| [**variables**](enum.md)                   |
| \[[**importlib**](importlib.md)\]     |
| [**interface**](interface.md)         |
| [**Bibliothèque**](library.md)             |
| [**modules**](module.md)               |
| [**modélis**](struct.md)               |
| [**typedef**](typedef.md)             |
| [**UE**](union.md)                 |



 

Pour plus d’informations sur la façon de marshaler des types OLE Automation, tels que **BSTR**, **Variant** et **SAFEARRAY**, consultez [marshaling de types de données OLE](marshaling-ole-data-types.md).

 

 




