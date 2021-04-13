---
title: entry (attribut)
description: L’attribut \ Entry \ spécifie une fonction ou une constante exportée dans un module en identifiant le point d’entrée dans la DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- MIDL (attribut d’entrée)
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314742"
---
# <a name="entry-attribute"></a>entry (attribut)

L’attribut **\[ entry \]** spécifie une fonction ou une constante exportée dans un module en identifiant le point d’entrée dans la dll.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour le [**module**](module.md).

</dd> <dt>

*ID d’entrée* 
</dt> <dd>

Spécifie le nom de la fonction de point d’entrée du module ou le numéro d’identification de l’entier.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs à appliquer au [**module**](module.md)par le compilateur MIDL.

</dd> <dt>

*NomModule* 
</dt> <dd>

Spécifie le nom que les autres composants logiciels utilisent pour désigner le [**module**](module.md).

</dd> <dt>

*elementlist* 
</dt> <dd>

Spécifie une ou plusieurs instructions de définition d’élément de module.

</dd> </dl>

## <a name="remarks"></a>Notes

Si la variable *EntryID* de l’attribut **\[ entry \]** est une chaîne, il s’agit d’un point d’entrée nommé. Si *EntryID* est un nombre, le point d’entrée est défini par un ordinal. Cet attribut fournit un moyen d’obtenir l’adresse d’une fonction dans un module.

## <a name="examples"></a>Exemples

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DllName**](dllname-str-.md)
</dt> <dt>

[**modules**](module.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 