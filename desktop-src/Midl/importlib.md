---
title: importlib (attribut)
description: La directive \ importlib \ rend les types qui ont déjà été compilés dans une autre bibliothèque de types disponible pour la bibliothèque de types en cours de création.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- MIDL de l’attribut importlib
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093489"
---
# <a name="importlib-attribute"></a>importlib (attribut)

La directive **\[ importlib \]** rend les types qui ont déjà été compilés dans une autre bibliothèque de types disponible pour la bibliothèque de types en cours de création.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Bibliothèque-attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs qui seront appliqués à la bibliothèque.

</dd> <dt>

*nom de la bibliothèque* 
</dt> <dd>

Identificateur que les composants logiciels utiliseront pour désigner cette [**bibliothèque**](library.md).

</dd> <dt>

*fichier à importer* 
</dt> <dd>

Nom et emplacement du fichier importé au moment de la compilation MIDL.

</dd> </dl>

## <a name="remarks"></a>Notes

Toutes les directives **\[ importlib \]** doivent précéder les autres descriptions de type dans la bibliothèque. Notez que la bibliothèque importée, ainsi que la bibliothèque générée, doivent être distribuées avec l’application afin d’être disponibles au moment de l’exécution.

Dans la plupart des cas, vous devez utiliser la **\[** [](import.md) **\]** directive d’importation MIDL pour référencer les définitions d’une autre. Fichier IDL dans votre. Fichier IDL. Cette méthode fournit à votre bibliothèque de types toutes les informations du fichier d’origine, tandis que **\[ importlib \]** affiche uniquement le contenu de la bibliothèque de types.

> [!Note]  
> La directive **\[ importlib \]** rend tout type défini dans la bibliothèque importée accessible à partir de la bibliothèque en cours de compilation. Pour éviter toute ambiguïté lorsqu’il existe des références en double, nous vous recommandons de qualifier chaque référence avec le nom de bibliothèque approprié, comme suit :

 

``` syntax
library_name.type
```

En l’absence de ces qualifications, MIDL résout l’ambiguïté des références dupliquées comme suit :

-   En vigueur avec la version 3,1, MIDL utilise la première référence qu’il trouve.
-   La version 3,0 de MIDL, la première version de MIDL qui pourrait générer des bibliothèques de types, utilise la dernière référence trouvée.

## <a name="examples"></a>Exemples

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[**port**](import.md)
</dt> <dt>

[Importation de fichiers d’en-tête système](importing-system-header-files.md)
</dt> <dt>

[Importation de fichiers et de bibliothèques de types](importing-files-and-type-libraries.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 