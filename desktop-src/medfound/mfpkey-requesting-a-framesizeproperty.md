---
description: Spécifie si l’encodeur doit utiliser une taille de trame préférée donnée dans le nombre d’échantillons par image.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544371"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="609d5-103">MFPKEY \_ demandant \_ une \_ propriété de trame</span><span class="sxs-lookup"><span data-stu-id="609d5-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="609d5-104">Spécifie si l’encodeur doit utiliser une taille de trame préférée donnée dans le nombre d’échantillons par image.</span><span class="sxs-lookup"><span data-stu-id="609d5-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="609d5-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="609d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="609d5-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="609d5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="609d5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="609d5-107">Data Type</span></span>

<span data-ttu-id="609d5-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="609d5-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="609d5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="609d5-109">Remarks</span></span>

<span data-ttu-id="609d5-110">Pour spécifier une taille de cadre préférée, définissez les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="609d5-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="609d5-111">Affectez à MFPKEY une valeur VARIANT pour une propriété de **\_ \_ \_ trame** \_ .</span><span class="sxs-lookup"><span data-stu-id="609d5-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="609d5-112">Définissez le cadre [**MFPKEY \_ préféré \_**](mfpkey-preferred-framesizeproperty.md) sur le nombre d’échantillons souhaité dans chaque image.</span><span class="sxs-lookup"><span data-stu-id="609d5-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="609d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="609d5-113">Requirements</span></span>



| <span data-ttu-id="609d5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="609d5-114">Requirement</span></span> | <span data-ttu-id="609d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="609d5-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="609d5-116">Client</span><span class="sxs-lookup"><span data-stu-id="609d5-116">Client</span></span><br/> | <span data-ttu-id="609d5-117">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="609d5-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="609d5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="609d5-118">Header</span></span><br/> | <dl> <span data-ttu-id="609d5-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="609d5-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609d5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="609d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609d5-121">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="609d5-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
