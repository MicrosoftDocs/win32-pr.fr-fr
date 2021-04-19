---
description: Définit la durée de la source du média en unités de 100 nanosecondes.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'IMFMediaSourceExtension :: SetDuration, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538262"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="a3737-103">IMFMediaSourceExtension :: SetDuration, méthode</span><span class="sxs-lookup"><span data-stu-id="a3737-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="a3737-104">Définit la durée de la source du média en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a3737-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3737-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3737-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="a3737-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3737-107">*durée* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3737-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3737-108">Durée de la source du média en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a3737-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3737-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3737-109">Return value</span></span>

<span data-ttu-id="a3737-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3737-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3737-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3737-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3737-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3737-112">Requirements</span></span>



| <span data-ttu-id="a3737-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3737-113">Requirement</span></span> | <span data-ttu-id="a3737-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3737-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3737-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3737-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a3737-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3737-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3737-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3737-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a3737-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3737-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a3737-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="a3737-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3737-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3737-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3737-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3737-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3737-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="a3737-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




