---
description: Supprime les segments de média définis par la plage de temps spécifiée du IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'IMFSourceBuffer :: Remove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527349"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="2519c-103">IMFSourceBuffer :: Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="2519c-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="2519c-104">Supprime les segments de média définis par la plage de temps spécifiée du [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="2519c-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="2519c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2519c-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="2519c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2519c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2519c-107">*Démarrer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2519c-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2519c-108">Début de l’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="2519c-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="2519c-109">*fin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2519c-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2519c-110">Fin de l’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="2519c-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2519c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2519c-111">Return value</span></span>

<span data-ttu-id="2519c-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2519c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2519c-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2519c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2519c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2519c-114">Requirements</span></span>



| <span data-ttu-id="2519c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2519c-115">Requirement</span></span> | <span data-ttu-id="2519c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2519c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2519c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2519c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2519c-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2519c-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2519c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2519c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2519c-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2519c-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2519c-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="2519c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2519c-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2519c-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2519c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2519c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2519c-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="2519c-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




