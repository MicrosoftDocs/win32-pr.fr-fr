---
description: Obtient un ID de session unique créé pour cette session.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'IMFMediaKeySession :: get_SessionId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531247"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="d372b-103">IMFMediaKeySession :: obtient \_ SessionID, méthode</span><span class="sxs-lookup"><span data-stu-id="d372b-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="d372b-104">Obtient un ID de session unique créé pour cette session.</span><span class="sxs-lookup"><span data-stu-id="d372b-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d372b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d372b-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="d372b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d372b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d372b-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="d372b-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="d372b-108">ID de session de la clé du support.</span><span class="sxs-lookup"><span data-stu-id="d372b-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d372b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d372b-109">Return value</span></span>

<span data-ttu-id="d372b-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d372b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d372b-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d372b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d372b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d372b-112">Requirements</span></span>



| <span data-ttu-id="d372b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d372b-113">Requirement</span></span> | <span data-ttu-id="d372b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d372b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d372b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d372b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d372b-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d372b-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d372b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d372b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d372b-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d372b-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d372b-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="d372b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d372b-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d372b-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d372b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d372b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d372b-122">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="d372b-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




