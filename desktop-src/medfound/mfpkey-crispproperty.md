---
description: Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755485"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="19461-103">\_Propriété Crisp MFPKEY</span><span class="sxs-lookup"><span data-stu-id="19461-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="19461-104">Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.</span><span class="sxs-lookup"><span data-stu-id="19461-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="19461-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="19461-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="19461-106">\_wszWMVCCrisp g</span><span class="sxs-lookup"><span data-stu-id="19461-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="19461-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="19461-107">Data Type</span></span>

<span data-ttu-id="19461-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="19461-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="19461-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="19461-109">Default Value</span></span>

<span data-ttu-id="19461-110">75</span><span class="sxs-lookup"><span data-stu-id="19461-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="19461-111">Notes</span><span class="sxs-lookup"><span data-stu-id="19461-111">Remarks</span></span>

<span data-ttu-id="19461-112">Cette valeur entière peut être comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="19461-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="19461-113">Plus la valeur est élevée, plus le codec optimise l’encodage pour la qualité d’image des trames individuelles, ce qui réduit généralement le lissage des mouvements.</span><span class="sxs-lookup"><span data-stu-id="19461-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="19461-114">Cette propriété doit être définie uniquement pour l’encodage CBR (constante-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="19461-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="19461-115">Les optimisations pour l’encodage VBR (variable-bit-rate) fonctionnent différemment.</span><span class="sxs-lookup"><span data-stu-id="19461-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="19461-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19461-116">Requirements</span></span>



| <span data-ttu-id="19461-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19461-117">Requirement</span></span> | <span data-ttu-id="19461-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="19461-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19461-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19461-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19461-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19461-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="19461-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19461-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19461-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19461-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19461-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="19461-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19461-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19461-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19461-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19461-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19461-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19461-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




