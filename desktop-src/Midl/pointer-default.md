---
title: pointer_default (attribut)
description: L’attribut \ pointeur \_ default \ spécifie l’attribut de pointeur par défaut pour tous les pointeurs, à l’exception des pointeurs de niveau supérieur qui apparaissent dans les listes de paramètres.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default MIDL de l’attribut
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031094"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="6792f-104">\_attribut par défaut du pointeur</span><span class="sxs-lookup"><span data-stu-id="6792f-104">pointer\_default attribute</span></span>

<span data-ttu-id="6792f-105">L’attribut **\[ \_ par \] défaut du pointeur** spécifie l’attribut de pointeur par défaut pour tous les pointeurs, à l’exception des pointeurs de niveau supérieur qui apparaissent dans les listes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="6792f-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="6792f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6792f-106">Parameters</span></span>

<span data-ttu-id="6792f-107">Cet attribut n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6792f-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="6792f-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="6792f-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="6792f-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6792f-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6792f-110">**interface**</span><span class="sxs-lookup"><span data-stu-id="6792f-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="6792f-111">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="6792f-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="6792f-112">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="6792f-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="6792f-113">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="6792f-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="6792f-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="6792f-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="6792f-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="6792f-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="6792f-116">**unique**</span><span class="sxs-lookup"><span data-stu-id="6792f-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="6792f-117">Types de pointeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="6792f-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 