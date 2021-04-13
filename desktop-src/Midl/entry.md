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
# <a name="entry-attribute"></a><span data-ttu-id="42dd6-104">entry (attribut)</span><span class="sxs-lookup"><span data-stu-id="42dd6-104">entry attribute</span></span>

<span data-ttu-id="42dd6-105">L’attribut **\[ entry \]** spécifie une fonction ou une constante exportée dans un module en identifiant le point d’entrée dans la dll.</span><span class="sxs-lookup"><span data-stu-id="42dd6-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="42dd6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42dd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dd6-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="42dd6-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd6-108">Spécifie un numéro d’identification unique universel pour le [**module**](module.md).</span><span class="sxs-lookup"><span data-stu-id="42dd6-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="42dd6-109">*ID d’entrée*</span><span class="sxs-lookup"><span data-stu-id="42dd6-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd6-110">Spécifie le nom de la fonction de point d’entrée du module ou le numéro d’identification de l’entier.</span><span class="sxs-lookup"><span data-stu-id="42dd6-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="42dd6-111">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="42dd6-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd6-112">Spécifie zéro, un ou plusieurs attributs à appliquer au [**module**](module.md)par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="42dd6-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="42dd6-113">*NomModule*</span><span class="sxs-lookup"><span data-stu-id="42dd6-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd6-114">Spécifie le nom que les autres composants logiciels utilisent pour désigner le [**module**](module.md).</span><span class="sxs-lookup"><span data-stu-id="42dd6-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="42dd6-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="42dd6-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="42dd6-116">Spécifie une ou plusieurs instructions de définition d’élément de module.</span><span class="sxs-lookup"><span data-stu-id="42dd6-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42dd6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="42dd6-117">Remarks</span></span>

<span data-ttu-id="42dd6-118">Si la variable *EntryID* de l’attribut **\[ entry \]** est une chaîne, il s’agit d’un point d’entrée nommé.</span><span class="sxs-lookup"><span data-stu-id="42dd6-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="42dd6-119">Si *EntryID* est un nombre, le point d’entrée est défini par un ordinal.</span><span class="sxs-lookup"><span data-stu-id="42dd6-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="42dd6-120">Cet attribut fournit un moyen d’obtenir l’adresse d’une fonction dans un module.</span><span class="sxs-lookup"><span data-stu-id="42dd6-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="42dd6-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="42dd6-121">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="42dd6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42dd6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dd6-123">**DllName**</span><span class="sxs-lookup"><span data-stu-id="42dd6-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="42dd6-124">**modules**</span><span class="sxs-lookup"><span data-stu-id="42dd6-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="42dd6-125">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="42dd6-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="42dd6-126">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="42dd6-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="42dd6-127">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="42dd6-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 