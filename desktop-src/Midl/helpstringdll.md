---
title: attribut helpstringdll
description: L’attribut \ helpstringdll \ définit le nom de la DLL à utiliser pour effectuer une recherche de chaîne de document.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- MIDL de l’attribut helpstringdll
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940890"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="fe6f6-104">attribut helpstringdll</span><span class="sxs-lookup"><span data-stu-id="fe6f6-104">helpstringdll attribute</span></span>

<span data-ttu-id="fe6f6-105">L’attribut **\[ helpstringdll \]** définit le nom de la dll à utiliser pour effectuer une recherche de chaîne de document.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="fe6f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe6f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6f6-107">*Help-Text-String*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6f6-108">Chaîne de caractères se terminant par zéro qui spécifie le nom de fichier complet d’une DLL.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f6-109">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6f6-110">Autres attributs qui s’appliquent à l’instruction Library dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="fe6f6-111">*nom de la bibliothèque*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6f6-112">Identificateur que les composants logiciels utiliseront pour désigner cette [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="fe6f6-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe6f6-113">*Bibliothèque-définition-instructions*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6f6-114">Une ou plusieurs instructions MIDL qui définissent l’interface de la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="fe6f6-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe6f6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fe6f6-115">Remarks</span></span>

<span data-ttu-id="fe6f6-116">Utilisez l’attribut **\[ helpstringdll \]** sur une instruction Library pour spécifier, sous la forme d’une chaîne de caractères, le nom de fichier complet d’une bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="fe6f6-117">Cela permet à un utilisateur d’afficher une description de la DLL avec l’Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="fe6f6-118">Utilisez les fonctions **GetDocumentation2** dans les interfaces **ITypeLib2** et **ITypeInfo2** pour récupérer la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe6f6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe6f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6f6-120">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="fe6f6-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="fe6f6-121">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fe6f6-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fe6f6-122">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fe6f6-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fe6f6-123">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="fe6f6-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 