---
description: Indique que la fin du flux multimédia a été atteinte.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'IMFMediaSourceExtension :: SetEndOfStream, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523107"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="ebe35-103">IMFMediaSourceExtension :: SetEndOfStream, méthode</span><span class="sxs-lookup"><span data-stu-id="ebe35-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="ebe35-104">Indique que la fin du flux multimédia a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="ebe35-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe35-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="ebe35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe35-107">*erreur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebe35-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe35-108">Utilisé pour transmettre les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ebe35-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe35-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebe35-109">Return value</span></span>

<span data-ttu-id="ebe35-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ebe35-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ebe35-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebe35-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe35-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe35-112">Requirements</span></span>



| <span data-ttu-id="ebe35-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebe35-113">Requirement</span></span> | <span data-ttu-id="ebe35-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebe35-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe35-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe35-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe35-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe35-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ebe35-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe35-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe35-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe35-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ebe35-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="ebe35-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ebe35-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ebe35-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe35-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe35-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="ebe35-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="ebe35-123">**\_erreur de MSE MF \_**</span><span class="sxs-lookup"><span data-stu-id="ebe35-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




