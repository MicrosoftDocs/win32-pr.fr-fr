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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462970"
---
# <a name="importlib-attribute"></a><span data-ttu-id="d224a-104">importlib (attribut)</span><span class="sxs-lookup"><span data-stu-id="d224a-104">importlib attribute</span></span>

<span data-ttu-id="d224a-105">La directive **\[ importlib \]** rend les types qui ont déjà été compilés dans une autre bibliothèque de types disponible pour la bibliothèque de types en cours de création.</span><span class="sxs-lookup"><span data-stu-id="d224a-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="d224a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d224a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d224a-107">*Bibliothèque-attributs*</span><span class="sxs-lookup"><span data-stu-id="d224a-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d224a-108">Zéro, un ou plusieurs attributs qui seront appliqués à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d224a-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="d224a-109">*nom de la bibliothèque*</span><span class="sxs-lookup"><span data-stu-id="d224a-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d224a-110">Identificateur que les composants logiciels utiliseront pour désigner cette [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="d224a-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d224a-111">*fichier à importer*</span><span class="sxs-lookup"><span data-stu-id="d224a-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="d224a-112">Nom et emplacement du fichier importé au moment de la compilation MIDL.</span><span class="sxs-lookup"><span data-stu-id="d224a-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d224a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d224a-113">Remarks</span></span>

<span data-ttu-id="d224a-114">Toutes les directives **\[ importlib \]** doivent précéder les autres descriptions de type dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d224a-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="d224a-115">Notez que la bibliothèque importée, ainsi que la bibliothèque générée, doivent être distribuées avec l’application afin d’être disponibles au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d224a-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="d224a-116">Dans la plupart des cas, vous devez utiliser la **\[** [](import.md) **\]** directive d’importation MIDL pour référencer les définitions d’une autre. Fichier IDL dans votre. Fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d224a-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="d224a-117">Cette méthode fournit à votre bibliothèque de types toutes les informations du fichier d’origine, tandis que **\[ importlib \]** affiche uniquement le contenu de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="d224a-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="d224a-118">La directive **\[ importlib \]** rend tout type défini dans la bibliothèque importée accessible à partir de la bibliothèque en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="d224a-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="d224a-119">Pour éviter toute ambiguïté lorsqu’il existe des références en double, nous vous recommandons de qualifier chaque référence avec le nom de bibliothèque approprié, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d224a-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="d224a-120">En l’absence de ces qualifications, MIDL résout l’ambiguïté des références dupliquées comme suit :</span><span class="sxs-lookup"><span data-stu-id="d224a-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="d224a-121">En vigueur avec la version 3,1, MIDL utilise la première référence qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="d224a-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="d224a-122">La version 3,0 de MIDL, la première version de MIDL qui pourrait générer des bibliothèques de types, utilise la dernière référence trouvée.</span><span class="sxs-lookup"><span data-stu-id="d224a-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="d224a-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="d224a-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="d224a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d224a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d224a-125">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="d224a-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="d224a-126">**port**</span><span class="sxs-lookup"><span data-stu-id="d224a-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="d224a-127">Importation de fichiers d’en-tête système</span><span class="sxs-lookup"><span data-stu-id="d224a-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="d224a-128">Importation de fichiers et de bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="d224a-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="d224a-129">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="d224a-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d224a-130">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="d224a-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d224a-131">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="d224a-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 