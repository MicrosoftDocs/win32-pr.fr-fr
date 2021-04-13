---
title: Constantes du journal des événements Windows (WinEvt. h)
description: 'Le journal des événements Windows définit les constantes suivantes :'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384612"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="e30de-103">Constantes du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="e30de-103">Windows Event Log Constants</span></span>

<span data-ttu-id="e30de-104">Le journal des événements Windows définit les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e30de-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="e30de-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_masque de \_ type \_ Variant evt**</span><span class="sxs-lookup"><span data-stu-id="e30de-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="e30de-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="e30de-107">Masque de bits que vous utilisez pour masquer le bit de tableau du type Variant, afin de pouvoir déterminer le type de données de la valeur variant contenue dans la structure de [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .</span><span class="sxs-lookup"><span data-stu-id="e30de-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e30de-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_tableau de \_ type \_ Variant evt**</span><span class="sxs-lookup"><span data-stu-id="e30de-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-109">128</span><span class="sxs-lookup"><span data-stu-id="e30de-109">128</span></span>
</dt> <dt>



<span data-ttu-id="e30de-110">Ce bit est défini pour le membre de **type** de la structure de la [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) si le variant contient un pointeur vers un tableau de valeurs, plutôt que la valeur elle-même.</span><span class="sxs-lookup"><span data-stu-id="e30de-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e30de-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_accès en lecture \_ à evt**</span><span class="sxs-lookup"><span data-stu-id="e30de-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-112">0x1</span><span class="sxs-lookup"><span data-stu-id="e30de-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="e30de-113">Autorisation de lecture de contrôle d’accès qui permet la lecture d’informations à partir d’un journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e30de-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e30de-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_accès en écriture \_ à evt**</span><span class="sxs-lookup"><span data-stu-id="e30de-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-115">0x2</span><span class="sxs-lookup"><span data-stu-id="e30de-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="e30de-116">Autorisation écrire le contrôle d’accès qui permet d’écrire des informations dans un journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e30de-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e30de-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT- \_ effacer \_ l’accès**</span><span class="sxs-lookup"><span data-stu-id="e30de-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-118">0x4</span><span class="sxs-lookup"><span data-stu-id="e30de-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="e30de-119">Désactivez l’autorisation de contrôle d’accès qui autorise l’effacement de toutes les informations d’un journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e30de-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e30de-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ tout \_ accès**</span><span class="sxs-lookup"><span data-stu-id="e30de-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e30de-121">0x7</span><span class="sxs-lookup"><span data-stu-id="e30de-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="e30de-122">Autorisation de contrôle d’accès All (lire, écrire, effacer et supprimer).</span><span class="sxs-lookup"><span data-stu-id="e30de-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e30de-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e30de-123">Requirements</span></span>



| <span data-ttu-id="e30de-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e30de-124">Requirement</span></span> | <span data-ttu-id="e30de-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e30de-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e30de-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e30de-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e30de-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e30de-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e30de-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e30de-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e30de-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e30de-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e30de-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e30de-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e30de-131"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e30de-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





