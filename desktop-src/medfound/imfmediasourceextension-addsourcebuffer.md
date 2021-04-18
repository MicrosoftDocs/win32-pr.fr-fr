---
description: Ajoute un IMFSourceBuffer à la collection de mémoires tampons associée au IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'IMFMediaSourceExtension :: AddSourceBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106520232"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="49993-103">IMFMediaSourceExtension :: AddSourceBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="49993-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="49993-104">Ajoute un [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) à la collection de mémoires tampons associée au [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span><span class="sxs-lookup"><span data-stu-id="49993-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="49993-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49993-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="49993-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49993-107">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49993-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="49993-108">*pNotify* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49993-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="49993-109">*ppSourceBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49993-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="49993-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="49993-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="49993-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49993-111">Return value</span></span>

<span data-ttu-id="49993-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49993-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49993-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49993-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49993-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49993-114">Requirements</span></span>



| <span data-ttu-id="49993-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49993-115">Requirement</span></span> | <span data-ttu-id="49993-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="49993-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49993-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49993-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49993-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49993-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="49993-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49993-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49993-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49993-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="49993-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="49993-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49993-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49993-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49993-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49993-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49993-124">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="49993-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




