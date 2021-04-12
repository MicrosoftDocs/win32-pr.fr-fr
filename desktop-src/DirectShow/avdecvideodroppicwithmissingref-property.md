---
description: Spécifie si le décodeur supprime les trames intra avec des frames de référence manquants.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propriété AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200722"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="19228-103">Propriété AVDecVideoDropPicWithMissingRef</span><span class="sxs-lookup"><span data-stu-id="19228-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="19228-104">Spécifie si le décodeur supprime les trames intra avec des frames de référence manquants.</span><span class="sxs-lookup"><span data-stu-id="19228-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="19228-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="19228-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="19228-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="19228-106">Data type</span></span>

<span data-ttu-id="19228-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="19228-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="19228-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="19228-108">Property GUID</span></span>

<span data-ttu-id="19228-109">**CODECAPI \_ AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="19228-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="19228-110">Notes</span><span class="sxs-lookup"><span data-stu-id="19228-110">Remarks</span></span>

<span data-ttu-id="19228-111">Si le flux binaire est endommagé, il est possible qu’il manque des frames de référence dans une trame.</span><span class="sxs-lookup"><span data-stu-id="19228-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="19228-112">Si la valeur de cette propriété est **\_ true**, le décodeur supprime le frame.</span><span class="sxs-lookup"><span data-stu-id="19228-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="19228-113">Si la valeur est **\_ false**, le décodeur tente de décoder le frame, en utilisant un ou plusieurs frames proches comme frames de référence.</span><span class="sxs-lookup"><span data-stu-id="19228-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="19228-114">L’image décodée résultante aura des artefacts de blocage.</span><span class="sxs-lookup"><span data-stu-id="19228-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="19228-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19228-115">Requirements</span></span>



| <span data-ttu-id="19228-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19228-116">Requirement</span></span> | <span data-ttu-id="19228-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="19228-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19228-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19228-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19228-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="19228-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="19228-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19228-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19228-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="19228-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="19228-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="19228-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="19228-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19228-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19228-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19228-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19228-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="19228-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="19228-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="19228-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




