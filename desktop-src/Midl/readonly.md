---
title: attribut en lecture seule
description: L’attribut \ ReadOnly \ interdit l’assignation à une variable.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- MIDL d’attribut ReadOnly
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940942"
---
# <a name="readonly-attribute"></a><span data-ttu-id="af07d-104">attribut en lecture seule</span><span class="sxs-lookup"><span data-stu-id="af07d-104">readonly attribute</span></span>

<span data-ttu-id="af07d-105">L’attribut **\[ ReadOnly \]** interdit l’assignation à une variable.</span><span class="sxs-lookup"><span data-stu-id="af07d-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="af07d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af07d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af07d-107">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="af07d-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="af07d-108">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="af07d-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="af07d-109">*type de données*</span><span class="sxs-lookup"><span data-stu-id="af07d-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="af07d-110">Type des données contenues par l' *identificateur*.</span><span class="sxs-lookup"><span data-stu-id="af07d-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="af07d-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="af07d-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="af07d-112">Nom par lequel le logiciel peut faire référence à l’emplacement de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="af07d-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af07d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="af07d-113">Remarks</span></span>

<span data-ttu-id="af07d-114">L’attribut **\[ ReadOnly \]** interdit l’assignation à une variable.</span><span class="sxs-lookup"><span data-stu-id="af07d-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="af07d-115">la **\[ lecture \]** seule est prise en charge uniquement au niveau du paramètre, et non au niveau de la méthode.</span><span class="sxs-lookup"><span data-stu-id="af07d-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="af07d-116">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="af07d-116">Flags</span></span>

<span data-ttu-id="af07d-117">VARFLAG \_ FREADONLY</span><span class="sxs-lookup"><span data-stu-id="af07d-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="af07d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="af07d-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="af07d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af07d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af07d-120">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="af07d-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="af07d-121">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="af07d-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="af07d-122">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="af07d-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="af07d-123">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="af07d-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 