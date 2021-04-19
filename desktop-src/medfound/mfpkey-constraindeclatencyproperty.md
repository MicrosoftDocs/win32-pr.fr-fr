---
description: Spécifie si l’encodeur est limité par une latence maximale de décodeur.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: MFPKEY_CONSTRAINDECLATENCY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521517"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="e3145-103">MFPKEY \_ propriété CONSTRAINDECLATENCY</span><span class="sxs-lookup"><span data-stu-id="e3145-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="e3145-104">Spécifie si l’encodeur est limité par une latence maximale de décodeur.</span><span class="sxs-lookup"><span data-stu-id="e3145-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3145-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e3145-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3145-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e3145-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3145-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e3145-107">Data Type</span></span>

<span data-ttu-id="e3145-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="e3145-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e3145-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e3145-109">Default Value</span></span>

<span data-ttu-id="e3145-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="e3145-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3145-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e3145-111">Remarks</span></span>

<span data-ttu-id="e3145-112">Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur énumère un ensemble de modes par défaut qui ont environ 1500 millisecondes de latence de décodeur.</span><span class="sxs-lookup"><span data-stu-id="e3145-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="e3145-113">Si vous affectez à cette propriété la **\_ valeur variant true**, vous devez également spécifier une latence maximale de décodeur en définissant la propriété [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e3145-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="e3145-114">Dans ce cas, l’encodeur crée des modes qui répondent aux exigences de latence et énumère uniquement ces modes.</span><span class="sxs-lookup"><span data-stu-id="e3145-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="e3145-115">L’encodeur garantit que les spécifications de la préroll (taille de mémoire tampon du décodeur) sont inférieures ou égales à **MFPKEY \_ MAXDECLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="e3145-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3145-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3145-116">Requirements</span></span>



| <span data-ttu-id="e3145-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3145-117">Requirement</span></span> | <span data-ttu-id="e3145-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3145-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3145-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3145-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3145-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3145-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3145-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3145-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3145-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3145-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3145-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3145-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3145-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3145-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3145-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3145-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3145-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3145-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
