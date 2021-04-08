---
description: Spécifie la date de la dernière modification d’un flux d’octets.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: Attribut MF_BYTESTREAM_LAST_MODIFIED_TIME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754284"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="17a00-103">\_Attribut d' \_ heure de dernière \_ modification de BYTESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="17a00-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="17a00-104">Spécifie la date de la dernière modification d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="17a00-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="17a00-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="17a00-105">Data type</span></span>

<span data-ttu-id="17a00-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="17a00-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="17a00-107">Notes</span><span class="sxs-lookup"><span data-stu-id="17a00-107">Remarks</span></span>

<span data-ttu-id="17a00-108">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="17a00-108">This attribute is optional.</span></span> <span data-ttu-id="17a00-109">La valeur de l’attribut est une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="17a00-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="17a00-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="17a00-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a00-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17a00-111">Requirements</span></span>



| <span data-ttu-id="17a00-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17a00-112">Requirement</span></span> | <span data-ttu-id="17a00-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="17a00-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a00-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a00-114">Minimum supported client</span></span><br/> | <span data-ttu-id="17a00-115">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="17a00-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="17a00-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a00-116">Minimum supported server</span></span><br/> | <span data-ttu-id="17a00-117">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="17a00-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="17a00-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="17a00-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a00-119"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17a00-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a00-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17a00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a00-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17a00-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="17a00-122">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="17a00-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="17a00-123">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="17a00-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="17a00-124">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="17a00-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="17a00-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="17a00-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
