---
description: Spécifie la matrice de canal, qui est utilisée pour convertir les canaux sources en canaux de destination (par exemple, pour convertir 5,1 en stéréo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521503"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="5c950-103">MFPKEY \_ WMRESAMP \_ CHANNELMTX, propriété</span><span class="sxs-lookup"><span data-stu-id="5c950-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="5c950-104">Spécifie la matrice de canal, qui est utilisée pour convertir les canaux sources en canaux de destination (par exemple, pour convertir 5,1 en stéréo).</span><span class="sxs-lookup"><span data-stu-id="5c950-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5c950-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5c950-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5c950-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5c950-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5c950-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="5c950-107">Data Type</span></span>

<span data-ttu-id="5c950-108">\_Tableau VT I4 \| VT \_</span><span class="sxs-lookup"><span data-stu-id="5c950-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="5c950-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="5c950-109">Applies To</span></span>

-   [<span data-ttu-id="5c950-110">Modèle de rééchantillonnage audio DSP</span><span class="sxs-lookup"><span data-stu-id="5c950-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="5c950-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5c950-111">Remarks</span></span>

<span data-ttu-id="5c950-112">La valeur de la propriété est une matrice de coefficients NS x ND, où ns est le nombre de canaux sources et ND le nombre de canaux de destination.</span><span class="sxs-lookup"><span data-stu-id="5c950-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="5c950-113">Les coefficients sont spécifiés en décibels à l’aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="5c950-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="5c950-114">tiers (65536 \* 20 \* log10 (dB))</span><span class="sxs-lookup"><span data-stu-id="5c950-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="5c950-115">La matrice est stockée sous la forme d’un tableau dans l’ordre ligne-principal, où le numéro de ligne est le canal source et le numéro de colonne est le canal de destination.</span><span class="sxs-lookup"><span data-stu-id="5c950-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="5c950-116">Par conséquent, si la matrice est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5c950-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="5c950-117">vous devez ensuite spécifier le tableau comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c950-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="5c950-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c950-118">Requirements</span></span>



| <span data-ttu-id="5c950-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c950-119">Requirement</span></span> | <span data-ttu-id="5c950-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c950-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c950-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c950-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c950-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c950-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5c950-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c950-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c950-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c950-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c950-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c950-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c950-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c950-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c950-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c950-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c950-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c950-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
