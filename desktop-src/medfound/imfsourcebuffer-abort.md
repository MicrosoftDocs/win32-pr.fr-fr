---
description: Abandonne le traitement du segment de média actuel.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'IMFSourceBuffer :: Abort, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527681"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="7da92-103">IMFSourceBuffer :: Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="7da92-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="7da92-104">Abandonne le traitement du segment de média actuel.</span><span class="sxs-lookup"><span data-stu-id="7da92-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7da92-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="7da92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7da92-106">Parameters</span></span>

<span data-ttu-id="7da92-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7da92-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7da92-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7da92-108">Return value</span></span>

<span data-ttu-id="7da92-109">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7da92-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7da92-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7da92-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da92-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7da92-111">Requirements</span></span>



| <span data-ttu-id="7da92-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7da92-112">Requirement</span></span> | <span data-ttu-id="7da92-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7da92-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da92-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da92-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7da92-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7da92-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7da92-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da92-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7da92-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7da92-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7da92-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="7da92-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7da92-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7da92-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da92-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da92-121">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="7da92-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




