---
description: Obtient l’état d’erreur associé à la session de la clé de média.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'IMFMediaKeySession :: GetError, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525804"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="9f54c-103">IMFMediaKeySession :: GetError, méthode</span><span class="sxs-lookup"><span data-stu-id="9f54c-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="9f54c-104">Obtient l’état d’erreur associé à la session de la clé de média.</span><span class="sxs-lookup"><span data-stu-id="9f54c-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f54c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f54c-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="9f54c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f54c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f54c-107">*code*</span><span class="sxs-lookup"><span data-stu-id="9f54c-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="9f54c-108">Code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="9f54c-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="9f54c-109">*systemCode*</span><span class="sxs-lookup"><span data-stu-id="9f54c-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="9f54c-110">Informations d’erreur spécifiques à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="9f54c-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f54c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f54c-111">Return value</span></span>

<span data-ttu-id="9f54c-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9f54c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f54c-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f54c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f54c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f54c-114">Requirements</span></span>



| <span data-ttu-id="9f54c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f54c-115">Requirement</span></span> | <span data-ttu-id="9f54c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f54c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f54c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f54c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f54c-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f54c-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f54c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f54c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f54c-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f54c-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9f54c-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="9f54c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f54c-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f54c-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f54c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f54c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f54c-124">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="9f54c-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




