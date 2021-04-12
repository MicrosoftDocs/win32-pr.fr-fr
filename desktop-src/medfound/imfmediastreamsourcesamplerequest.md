---
description: Représente une demande pour un exemple à partir d’un source.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interface IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321581"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="0f3a2-103">Interface IMFMediaStreamSourceSampleRequest</span><span class="sxs-lookup"><span data-stu-id="0f3a2-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="0f3a2-104">Représente une demande pour un exemple à partir d’un source.</span><span class="sxs-lookup"><span data-stu-id="0f3a2-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="0f3a2-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0f3a2-105">Members</span></span>

<span data-ttu-id="0f3a2-106">L’interface **IMFMediaStreamSourceSampleRequest** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0f3a2-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0f3a2-107">**IMFMediaStreamSourceSampleRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0f3a2-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="0f3a2-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f3a2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0f3a2-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f3a2-109">Methods</span></span>

<span data-ttu-id="0f3a2-110">L’interface **IMFMediaStreamSourceSampleRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0f3a2-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="0f3a2-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0f3a2-111">Method</span></span>                                                           | <span data-ttu-id="0f3a2-112">Description</span><span class="sxs-lookup"><span data-stu-id="0f3a2-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="0f3a2-113">**SetSample**</span><span class="sxs-lookup"><span data-stu-id="0f3a2-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="0f3a2-114">Définit l’exemple pour la source du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="0f3a2-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f3a2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0f3a2-115">Remarks</span></span>

<span data-ttu-id="0f3a2-116">**MFMediaStreamSourceSampleRequest** est implémenté par la classe Runtime [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="0f3a2-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3a2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f3a2-117">Requirements</span></span>



| <span data-ttu-id="0f3a2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f3a2-118">Requirement</span></span> | <span data-ttu-id="0f3a2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f3a2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3a2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3a2-121">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0f3a2-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0f3a2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3a2-123">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0f3a2-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="0f3a2-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f3a2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f3a2-125"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f3a2-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3a2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f3a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3a2-127">Interfaces Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f3a2-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
