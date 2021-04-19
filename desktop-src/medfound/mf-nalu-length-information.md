---
description: Indique les longueurs de NALUs dans l’exemple. Il s’agit d’un objet BLOB MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Attribut MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517654"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="37514-104">\_Attribut d' \_ information de longueur Nalu MF \_</span><span class="sxs-lookup"><span data-stu-id="37514-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="37514-105">Indique les longueurs de NALUs dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="37514-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="37514-106">Il s’agit d’un **objet BLOB** MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 264.</span><span class="sxs-lookup"><span data-stu-id="37514-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="37514-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="37514-107">Data type</span></span>

<span data-ttu-id="37514-108">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="37514-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="37514-109">Notes</span><span class="sxs-lookup"><span data-stu-id="37514-109">Remarks</span></span>

<span data-ttu-id="37514-110">Pour que cet attribut soit défini, le support doit être de type MEDIASUBTYPE \_ H264 – et l’attribut [set de \_ \_ longueur \_ Nalu MF](mf-nalu-length-set.md) doit être défini sur le type de média d’entrée de MEDIASUBTYPE \_ H264 –.</span><span class="sxs-lookup"><span data-stu-id="37514-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="37514-111">Définissez les \_ informations de longueur Nalu MF \_ \_ en tant qu' **objet BLOB** sur l’exemple d’entrée, avec un DWORD pour chaque Nalu dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="37514-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="37514-112">Par exemple, s’il existe AUD (9 octets), SPS (25 octets), PPS (10 octets), slice1 (50 k), r tranche 2 (60 k), il doit y avoir 5 DWORDs avec les valeurs 9, 25, 10, 50 k, 60 k dans l' **objet BLOB**.</span><span class="sxs-lookup"><span data-stu-id="37514-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="37514-113">Ici, du code qui définit l' **objet BLOB**, où **rgdwNALULengthInfo** est un tableau de type DWORD et **uiNaluLengthIdx** les longueurs Nalu valides définies sur l' **objet BLOB**.</span><span class="sxs-lookup"><span data-stu-id="37514-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="37514-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37514-114">Requirements</span></span>



| <span data-ttu-id="37514-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37514-115">Requirement</span></span> | <span data-ttu-id="37514-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="37514-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37514-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37514-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37514-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="37514-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="37514-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37514-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37514-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="37514-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="37514-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="37514-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="37514-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37514-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37514-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37514-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37514-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37514-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37514-125">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="37514-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




