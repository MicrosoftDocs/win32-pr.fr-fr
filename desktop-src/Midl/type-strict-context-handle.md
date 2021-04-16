---
title: attribut type_strict_context_handle
description: Utilisez le gestionnaire de \_ contexte \ type strict \_ \_ \ dans un fichier ACF pour définir des restrictions sur les handles de contexte.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462982"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="d745d-104">\_attribut de \_ handle de contexte strict \_</span><span class="sxs-lookup"><span data-stu-id="d745d-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="d745d-105">Utilisez le **\[ type \_ strict \_ \_ handle \] de contexte** dans un fichier ACF pour définir des restrictions sur les handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="d745d-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="d745d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d745d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d745d-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="d745d-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d745d-108">Autres attributs ACF qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d745d-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="d745d-109">Les attributs valides incluent le [**\_ descripteur automatique**](auto-handle.md), le [**\_ handle implicite**](implicit-handle.md), le [**\_ handle explicite**](explicit-handle.md)et l' [**optimisation**](optimize.md), le [**code**](code.md)ou le [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="d745d-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="d745d-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d745d-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d745d-111">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="d745d-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d745d-112">Nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d745d-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d745d-113">*interface-définition-instructions*</span><span class="sxs-lookup"><span data-stu-id="d745d-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="d745d-114">Une ou plusieurs instructions MIDL qui définissent les éléments de l' [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="d745d-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d745d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d745d-115">Remarks</span></span>

<span data-ttu-id="d745d-116">Pour pouvoir utiliser cet attribut, l’indicateur-target doit avoir la valeur NT60 (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d745d-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="d745d-117">\[\_le type \_ \_ de handle de contexte strict \] est un sur-ensemble fonctionnel du \[ handle de \_ contexte strict \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d745d-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="d745d-118">Dans \[ \_ un handle de contexte strict \_ \] , l’ID de type du descripteur est toujours 0 ; dans \[ le type de \_ handle de \_ contexte strict \_ \] , un ID de type unique est assigné par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="d745d-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="d745d-119">Il est recommandé d’utiliser \[ un \_ \_ handle de contexte strict \_ \] plutôt qu’un \[ handle de contexte strict \_ \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d745d-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="d745d-120">Les handles de contexte ne sont pas associés à un type spécifique par défaut.</span><span class="sxs-lookup"><span data-stu-id="d745d-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="d745d-121">Lorsque plusieurs types de handles de contexte sont utilisés dans le même processus, un client malveillant peut passer un handle de contexte à la place d’un autre pour produire des résultats indésirables.</span><span class="sxs-lookup"><span data-stu-id="d745d-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="d745d-122">L’utilisation du \[ \_ handle de \_ contexte \_ strict \] permet aux applications d’appliquer la cohérence des types de handles de contexte et d’empêcher toute utilisation incompatible de type de handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="d745d-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="d745d-123">Un handle de contexte attribué avec un \[ handle de contexte de type \_ strict \_ \_ \] ne peut pas également être attribué avec un \[ handle de \_ contexte strict \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d745d-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="d745d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d745d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d745d-125">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="d745d-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d745d-126">**code**</span><span class="sxs-lookup"><span data-stu-id="d745d-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="d745d-127">Handles de contexte</span><span class="sxs-lookup"><span data-stu-id="d745d-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="d745d-128">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="d745d-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="d745d-129">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="d745d-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="d745d-130">**\_handle explicite**</span><span class="sxs-lookup"><span data-stu-id="d745d-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d745d-131">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="d745d-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d745d-132">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="d745d-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="d745d-133">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="d745d-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="d745d-134">\_handle de contexte strict \_</span><span class="sxs-lookup"><span data-stu-id="d745d-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 