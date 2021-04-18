---
description: Spécifie le niveau de qualité souhaité pour l’encodage de flux audio (VBR) basé sur la qualité (1 passe).
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542925"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="10f4b-103">MFPKEY \_ \_ propriété VBRQUALITY souhaitée</span><span class="sxs-lookup"><span data-stu-id="10f4b-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="10f4b-104">Spécifie le niveau de qualité souhaité pour l’encodage de flux audio (VBR) basé sur la qualité (1 passe).</span><span class="sxs-lookup"><span data-stu-id="10f4b-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="10f4b-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="10f4b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="10f4b-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="10f4b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="10f4b-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="10f4b-107">Data Type</span></span>

<span data-ttu-id="10f4b-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="10f4b-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="10f4b-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="10f4b-109">Default Value</span></span>

<span data-ttu-id="10f4b-110">0</span><span class="sxs-lookup"><span data-stu-id="10f4b-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="10f4b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="10f4b-111">Remarks</span></span>

<span data-ttu-id="10f4b-112">Cette valeur peut être comprise entre 0 et 100, où 100 correspond à la qualité maximale.</span><span class="sxs-lookup"><span data-stu-id="10f4b-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="10f4b-113">La valeur 0 indique que la méthode d’encodage VBR basé sur la qualité ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="10f4b-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="10f4b-114">Pour énumérer les modes VBR qui répondent à un certain besoin de qualité, définissez les propriétés suivantes de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="10f4b-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="10f4b-115">Affectez à [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="10f4b-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="10f4b-116">Affectez à [**MFPKEY la \_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="10f4b-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="10f4b-117">Définissez **MFPKEY \_ \_ VBRQUALITY souhaité** sur la qualité souhaitée.</span><span class="sxs-lookup"><span data-stu-id="10f4b-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="10f4b-118">Pour les modes sans perte, définissez la qualité souhaitée sur 100.</span><span class="sxs-lookup"><span data-stu-id="10f4b-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f4b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10f4b-119">Requirements</span></span>



| <span data-ttu-id="10f4b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10f4b-120">Requirement</span></span> | <span data-ttu-id="10f4b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="10f4b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10f4b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10f4b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10f4b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10f4b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="10f4b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10f4b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10f4b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10f4b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10f4b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="10f4b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="10f4b-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10f4b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f4b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10f4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f4b-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10f4b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
