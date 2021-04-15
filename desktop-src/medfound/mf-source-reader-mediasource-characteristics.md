---
description: Obtient les caractéristiques de la source du média à partir du lecteur source.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Attribut MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321661"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="21199-103">Attribut des caractéristiques de l' \_ \_ \_ attribut MEDIASOURCE du lecteur source MF \_</span><span class="sxs-lookup"><span data-stu-id="21199-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="21199-104">Obtient les caractéristiques de la source du média à partir du [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="21199-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="21199-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="21199-105">Data type</span></span>

<span data-ttu-id="21199-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="21199-106">**UINT32**</span></span>

<span data-ttu-id="21199-107">La valeur est **une opération or** au niveau du bit des indicateurs de l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="21199-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="21199-108">Notes</span><span class="sxs-lookup"><span data-stu-id="21199-108">Remarks</span></span>

<span data-ttu-id="21199-109">Pour récupérer cet attribut, appelez la méthode [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) sur le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="21199-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="21199-110">Définissez le paramètre *dwStreamIndex* sur **MF \_ source \_ Reader \_ MediaSource** et le paramètre *guidAttribute* sur les \_ caractéristiques du lecteur source MF \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="21199-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="21199-111">Le type **PROPVARIANT** pour cet attribut est **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="21199-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="21199-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="21199-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="21199-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21199-113">Requirements</span></span>



| <span data-ttu-id="21199-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21199-114">Requirement</span></span> | <span data-ttu-id="21199-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="21199-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21199-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21199-116">Minimum supported client</span></span><br/> | <span data-ttu-id="21199-117">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="21199-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="21199-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21199-118">Minimum supported server</span></span><br/> | <span data-ttu-id="21199-119">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="21199-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="21199-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="21199-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="21199-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="21199-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21199-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21199-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21199-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21199-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="21199-124">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="21199-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




