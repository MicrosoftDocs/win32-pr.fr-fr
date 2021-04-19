---
description: Définit l’exemple pour la source du flux multimédia.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'IMFMediaStreamSourceSampleRequest :: SetSample, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525798"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="84957-103">IMFMediaStreamSourceSampleRequest :: SetSample, méthode</span><span class="sxs-lookup"><span data-stu-id="84957-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="84957-104">Définit l’exemple pour la source du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="84957-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="84957-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84957-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="84957-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84957-107">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84957-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84957-108">Exemple pour la source du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="84957-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84957-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84957-109">Return value</span></span>

<span data-ttu-id="84957-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="84957-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84957-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84957-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84957-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84957-112">Requirements</span></span>



| <span data-ttu-id="84957-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84957-113">Requirement</span></span> | <span data-ttu-id="84957-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="84957-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84957-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84957-115">Minimum supported client</span></span><br/> | <span data-ttu-id="84957-116">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84957-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="84957-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84957-117">Minimum supported server</span></span><br/> | <span data-ttu-id="84957-118">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84957-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="84957-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="84957-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84957-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84957-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84957-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84957-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84957-122">**IMFMediaStreamSourceSampleRequest**</span><span class="sxs-lookup"><span data-stu-id="84957-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




