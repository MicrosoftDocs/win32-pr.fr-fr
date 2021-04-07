---
title: helpfile (attribut)
description: L’attribut \ HelpFile \ définit le nom du fichier d’aide d’une bibliothèque de types. Tous les types d’une bibliothèque partagent le même fichier d’aide.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- attribut HelpFile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725164"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="3ef22-105">helpfile (attribut)</span><span class="sxs-lookup"><span data-stu-id="3ef22-105">helpfile attribute</span></span>

<span data-ttu-id="3ef22-106">L’attribut **\[ HelpFile \]** définit le nom du fichier d’aide d’une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="3ef22-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="3ef22-107">Tous les types d’une bibliothèque partagent le même fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="3ef22-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="3ef22-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ef22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef22-109">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="3ef22-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="3ef22-110">Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="3ef22-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ef22-111">*extension*</span><span class="sxs-lookup"><span data-stu-id="3ef22-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="3ef22-112">Spécifie le nom du fichier contenant le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="3ef22-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="3ef22-113">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3ef22-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3ef22-114">Spécifie zéro, un ou plusieurs attributs que le compilateur MIDL appliquera à la [**bibliothèque**](library.md).</span><span class="sxs-lookup"><span data-stu-id="3ef22-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ef22-115">*instructions de bibliothèque*</span><span class="sxs-lookup"><span data-stu-id="3ef22-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="3ef22-116">Spécifie une ou plusieurs instructions MIDL qui définissent l’interface de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3ef22-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ef22-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3ef22-117">Remarks</span></span>

<span data-ttu-id="3ef22-118">Utilisez les fonctions **GetDocumentation** dans les interfaces **ITypeLib** et **ITypeInfo** pour récupérer le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3ef22-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="3ef22-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="3ef22-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="3ef22-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ef22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef22-121">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="3ef22-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="3ef22-122">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="3ef22-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3ef22-123">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="3ef22-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3ef22-124">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="3ef22-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 