---
description: Spécifie le nombre d’échantillons par défaut par image.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: MFPKEY_PREFERRED_FRAMESIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526874"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="392d3-103">\_Propriété de \_ trame préférée MFPKEY</span><span class="sxs-lookup"><span data-stu-id="392d3-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="392d3-104">Spécifie le nombre d’échantillons par défaut par image.</span><span class="sxs-lookup"><span data-stu-id="392d3-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="392d3-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="392d3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="392d3-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="392d3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="392d3-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="392d3-107">Data Type</span></span>

<span data-ttu-id="392d3-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="392d3-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="392d3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="392d3-109">Remarks</span></span>

<span data-ttu-id="392d3-110">Pour spécifier une taille de cadre préférée, définissez les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="392d3-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="392d3-111">Affectez à MFPKEY une **\_ valeur variant** pour une propriété de [**\_ \_ \_ trame**](mfpkey-requesting-a-framesizeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="392d3-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="392d3-112">Définissez le cadre **MFPKEY \_ préféré \_** sur le nombre d’échantillons souhaité dans chaque image.</span><span class="sxs-lookup"><span data-stu-id="392d3-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="392d3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="392d3-113">Requirements</span></span>



| <span data-ttu-id="392d3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="392d3-114">Requirement</span></span> | <span data-ttu-id="392d3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="392d3-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="392d3-116">Client</span><span class="sxs-lookup"><span data-stu-id="392d3-116">Client</span></span><br/> | <span data-ttu-id="392d3-117">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="392d3-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="392d3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="392d3-118">Header</span></span><br/> | <dl> <span data-ttu-id="392d3-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="392d3-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="392d3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="392d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392d3-121">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="392d3-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
