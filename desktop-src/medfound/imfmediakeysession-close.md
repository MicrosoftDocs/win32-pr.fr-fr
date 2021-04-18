---
description: Ferme la session de clé de média et doit être appelée avant la libération de la session de clé.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'IMFMediaKeySession :: Close, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523103"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="fa8ca-103">IMFMediaKeySession :: Close, méthode</span><span class="sxs-lookup"><span data-stu-id="fa8ca-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="fa8ca-104">Ferme la session de clé de média et doit être appelée avant la libération de la session de clé.</span><span class="sxs-lookup"><span data-stu-id="fa8ca-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8ca-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="fa8ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa8ca-106">Parameters</span></span>

<span data-ttu-id="fa8ca-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fa8ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa8ca-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa8ca-108">Return value</span></span>

<span data-ttu-id="fa8ca-109">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa8ca-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa8ca-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa8ca-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8ca-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa8ca-111">Requirements</span></span>



| <span data-ttu-id="fa8ca-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa8ca-112">Requirement</span></span> | <span data-ttu-id="fa8ca-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa8ca-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8ca-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8ca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8ca-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8ca-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa8ca-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8ca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8ca-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8ca-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fa8ca-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="fa8ca-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa8ca-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa8ca-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa8ca-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa8ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8ca-121">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="fa8ca-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




