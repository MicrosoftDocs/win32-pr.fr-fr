---
title: Constantes du collecteur d’événements Windows (Evcoll. h)
description: Le kit de développement logiciel (SDK) du collecteur d’événements Windows contient les constantes suivantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739741"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="73307-103">Constantes du collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="73307-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="73307-104">Le kit de développement logiciel (SDK) du collecteur d’événements Windows contient les constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="73307-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="73307-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_masque de \_ type de variante EC \_**</span><span class="sxs-lookup"><span data-stu-id="73307-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="73307-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="73307-107">Utilisé pour masquer le bit du tableau de la propriété **type** d’une [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) pour extraire le type de la valeur variant.</span><span class="sxs-lookup"><span data-stu-id="73307-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_tableau de \_ type \_ Variant EC**</span><span class="sxs-lookup"><span data-stu-id="73307-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="73307-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="73307-110">Lorsque ce bit est défini dans la propriété **type** d’un [**\_ Variant EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), le variant contient un pointeur vers un tableau de valeurs, plutôt que la valeur elle-même.</span><span class="sxs-lookup"><span data-stu-id="73307-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_accès en lecture EC \_**</span><span class="sxs-lookup"><span data-stu-id="73307-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-112">1</span><span class="sxs-lookup"><span data-stu-id="73307-112">1</span></span>
</dt> <dt>



<span data-ttu-id="73307-113">Autorisation de lecture de contrôle d’accès qui permet la lecture d’informations à partir du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="73307-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_accès en écriture EC \_**</span><span class="sxs-lookup"><span data-stu-id="73307-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-115">2</span><span class="sxs-lookup"><span data-stu-id="73307-115">2</span></span>
</dt> <dt>



<span data-ttu-id="73307-116">Autorisation écrire le contrôle d’accès qui permet d’écrire des informations dans le collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="73307-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ Open \_ Always**</span><span class="sxs-lookup"><span data-stu-id="73307-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-118">0</span><span class="sxs-lookup"><span data-stu-id="73307-118">0</span></span>
</dt> <dt>



<span data-ttu-id="73307-119">Ouvre un abonnement existant ou crée l’abonnement s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="73307-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="73307-120">Utilisé par la méthode [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="73307-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_création \_ de EC**</span><span class="sxs-lookup"><span data-stu-id="73307-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-122">1</span><span class="sxs-lookup"><span data-stu-id="73307-122">1</span></span>
</dt> <dt>



<span data-ttu-id="73307-123">Indicateur passé à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) spécifiant qu’un nouvel abonnement doit être créé.</span><span class="sxs-lookup"><span data-stu-id="73307-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73307-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**\_Open EC \_ existant**</span><span class="sxs-lookup"><span data-stu-id="73307-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73307-125">2</span><span class="sxs-lookup"><span data-stu-id="73307-125">2</span></span>
</dt> <dt>



<span data-ttu-id="73307-126">Indicateur passé à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) spécifiant qu’un abonnement existant doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="73307-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73307-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73307-127">Requirements</span></span>



| <span data-ttu-id="73307-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73307-128">Requirement</span></span> | <span data-ttu-id="73307-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="73307-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="73307-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73307-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73307-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73307-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="73307-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73307-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73307-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73307-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="73307-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="73307-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="73307-135"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="73307-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





