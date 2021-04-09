---
title: attribut strict_context_handle
description: L’attribut \ \_ \_ ACF du handle de contexte \ CCP définit des restrictions sur les handles de contexte.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940865"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="0f4d7-104">attribut de handle de \_ contexte strict \_</span><span class="sxs-lookup"><span data-stu-id="0f4d7-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="0f4d7-105">Le **\[ strict \_ \_ handle \] de contexte** CCP définit des restrictions sur les handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="0f4d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f4d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f4d7-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0f4d7-108">Autres attributs ACF qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="0f4d7-109">Les attributs valides incluent le [**\_ descripteur automatique**](auto-handle.md), le [**\_ handle implicite**](implicit-handle.md), le [**\_ handle explicite**](explicit-handle.md)et l' [**optimisation**](optimize.md), le [**code**](code.md)ou le [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="0f4d7-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="0f4d7-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0f4d7-111">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0f4d7-112">Nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="0f4d7-113">*interface-définition-instructions*</span><span class="sxs-lookup"><span data-stu-id="0f4d7-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="0f4d7-114">Une ou plusieurs instructions MIDL qui définissent les éléments de l' [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="0f4d7-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f4d7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0f4d7-115">Remarks</span></span>

<span data-ttu-id="0f4d7-116">Normalement, lorsqu’un appel à une méthode d’interface génère un handle de contexte, ce descripteur devient librement disponible pour toute autre interface.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="0f4d7-117">Lorsque vous utilisez l’attribut de **\[ \_ \_ handle \] de contexte strict** , vous garantissez que les méthodes de cette interface acceptent uniquement les handles de contexte qui ont été créés par une méthode à partir de la même interface.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="0f4d7-118">Les interfaces compilées sans un **\[ \_ \_ handle \] de contexte strict** ne peuvent pas accepter des handles de contexte créés sur des interfaces compilées avec un **\[ \_ \_ \] handle de contexte strict**.</span><span class="sxs-lookup"><span data-stu-id="0f4d7-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f4d7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f4d7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f4d7-120">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="0f4d7-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-121">**code**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-122">Handles de contexte</span><span class="sxs-lookup"><span data-stu-id="0f4d7-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="0f4d7-123">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-124">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-125">**\_handle explicite**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-126">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-127">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-128">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="0f4d7-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="0f4d7-129">\_handle de \_ contexte \_ strict de type</span><span class="sxs-lookup"><span data-stu-id="0f4d7-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 