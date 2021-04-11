---
description: Supprime la mémoire tampon source spécifiée de la collection de mémoires tampons sources gérée par l’objet IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'IMFMediaSourceExtension :: RemoveSourceBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321582"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="3ecbf-103">IMFMediaSourceExtension :: RemoveSourceBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="3ecbf-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="3ecbf-104">Supprime la mémoire tampon source spécifiée de la collection de mémoires tampons sources gérée par l’objet [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .</span><span class="sxs-lookup"><span data-stu-id="3ecbf-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecbf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ecbf-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3ecbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ecbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ecbf-107">*pSourceBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ecbf-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ecbf-108">Mémoire tampon à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3ecbf-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ecbf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ecbf-109">Return value</span></span>

<span data-ttu-id="3ecbf-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3ecbf-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ecbf-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ecbf-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecbf-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ecbf-112">Requirements</span></span>



| <span data-ttu-id="3ecbf-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ecbf-113">Requirement</span></span> | <span data-ttu-id="3ecbf-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ecbf-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecbf-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecbf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecbf-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ecbf-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ecbf-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecbf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecbf-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ecbf-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3ecbf-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="3ecbf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ecbf-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ecbf-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecbf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ecbf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecbf-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="3ecbf-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




