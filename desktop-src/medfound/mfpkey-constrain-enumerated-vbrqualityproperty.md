---
description: Spécifie si les modes énumérés par l’encodeur sont Limeted à ceux qui répondent à une exigence de qualité donnée par MFPKEY \_ souhaité \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540091"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="ca343-103">MFPKEY \_ contraindre la \_ \_ propriété VBRQUALITY énumérée</span><span class="sxs-lookup"><span data-stu-id="ca343-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="ca343-104">Spécifie si les modes énumérés par l’encodeur sont Limeted à ceux qui répondent à une exigence de qualité donnée par [**MFPKEY \_ souhaité \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ca343-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ca343-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ca343-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ca343-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ca343-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ca343-107">Data Type</span></span>

<span data-ttu-id="ca343-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ca343-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="ca343-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ca343-109">Default Value</span></span>

<span data-ttu-id="ca343-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="ca343-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="ca343-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ca343-111">Remarks</span></span>

<span data-ttu-id="ca343-112">Pour énumérer les modes VBR qui répondent à un certain besoin de qualité, définissez les propriétés suivantes de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="ca343-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="ca343-113">Affectez à [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="ca343-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="ca343-114">Affectez à **MFPKEY la \_ contrainte \_ énumérée \_ VBRQUALITY** la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="ca343-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="ca343-115">Définissez [**MFPKEY \_ \_ VBRQUALITY souhaité**](mfpkey-desired-vbrqualityproperty.md) sur la qualité souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ca343-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="ca343-116">Pour les modes sans perte, définissez la qualité souhaitée sur 100.</span><span class="sxs-lookup"><span data-stu-id="ca343-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca343-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca343-117">Requirements</span></span>



| <span data-ttu-id="ca343-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca343-118">Requirement</span></span> | <span data-ttu-id="ca343-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca343-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca343-120">Client</span><span class="sxs-lookup"><span data-stu-id="ca343-120">Client</span></span><br/> | <span data-ttu-id="ca343-121">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca343-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="ca343-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca343-122">Header</span></span><br/> | <dl> <span data-ttu-id="ca343-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca343-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca343-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca343-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca343-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca343-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
