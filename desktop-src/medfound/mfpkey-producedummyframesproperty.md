---
description: Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: MFPKEY_PRODUCEDUMMYFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202339"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="10794-103">MFPKEY \_ propriété PRODUCEDUMMYFRAMES</span><span class="sxs-lookup"><span data-stu-id="10794-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="10794-104">Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.</span><span class="sxs-lookup"><span data-stu-id="10794-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="10794-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="10794-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="10794-106">\_wszWMVCProduceDummyFrames g</span><span class="sxs-lookup"><span data-stu-id="10794-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="10794-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="10794-107">Data Type</span></span>

<span data-ttu-id="10794-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="10794-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="10794-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="10794-109">Default Value</span></span>

<span data-ttu-id="10794-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="10794-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="10794-111">Notes</span><span class="sxs-lookup"><span data-stu-id="10794-111">Remarks</span></span>

<span data-ttu-id="10794-112">Si cette valeur est \_ false, le codec ne placera aucune donnée dans le flux binaire pour les trames dupliquées.</span><span class="sxs-lookup"><span data-stu-id="10794-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="10794-113">Les trames factices peuvent être importantes dans les applications où les numéros de trame sont conservés.</span><span class="sxs-lookup"><span data-stu-id="10794-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="10794-114">C’est le cas, par exemple, lorsque les codes de temps SMPTE sont conservés pour le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="10794-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="10794-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10794-115">Requirements</span></span>



| <span data-ttu-id="10794-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10794-116">Requirement</span></span> | <span data-ttu-id="10794-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="10794-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10794-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10794-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10794-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10794-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="10794-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10794-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10794-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10794-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10794-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="10794-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10794-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10794-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10794-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10794-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10794-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10794-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




