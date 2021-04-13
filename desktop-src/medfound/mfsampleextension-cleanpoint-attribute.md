---
description: Indique si un échantillon est un point d’accès aléatoire.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: Attribut MFSampleExtension_CleanPoint (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527946"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="c518d-103">\_Attribut MFSampleExtension CleanPoint</span><span class="sxs-lookup"><span data-stu-id="c518d-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="c518d-104">Indique si un échantillon est un point d’accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="c518d-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="c518d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c518d-105">Data type</span></span>

<span data-ttu-id="c518d-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c518d-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c518d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="c518d-107">Get/set</span></span>

<span data-ttu-id="c518d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c518d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c518d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c518d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c518d-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="c518d-110">Applies to</span></span>

[<span data-ttu-id="c518d-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="c518d-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="c518d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c518d-112">Remarks</span></span>

<span data-ttu-id="c518d-113">Cet attribut s’applique aux exemples.</span><span class="sxs-lookup"><span data-stu-id="c518d-113">This attribute applies to samples.</span></span> <span data-ttu-id="c518d-114">Si l’attribut a la **valeur true**, l’exemple est un point d’accès aléatoire et le décodage peut commencer à partir de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c518d-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="c518d-115">Dans le cas contraire, l’exemple n’est pas un point d’accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="c518d-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="c518d-116">Si cet attribut n’est pas défini, la valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="c518d-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="c518d-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c518d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="c518d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="c518d-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="c518d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c518d-119">Requirements</span></span>



| <span data-ttu-id="c518d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c518d-120">Requirement</span></span> | <span data-ttu-id="c518d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c518d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c518d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c518d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c518d-123">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c518d-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c518d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c518d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c518d-125">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="c518d-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c518d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c518d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c518d-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c518d-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c518d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c518d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c518d-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c518d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c518d-130">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="c518d-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c518d-131">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="c518d-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




