---
description: La suspension réelle est sur le point de se produire et aucun autre appel ne sera effectué dans le module de déchiffrement de contenu (CDM).
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'IMFCdmSuspendNotify :: end, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533846"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="33bc4-103">IMFCdmSuspendNotify :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="33bc4-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="33bc4-104">La suspension réelle est sur le point de se produire et aucun autre appel ne sera effectué dans le module de déchiffrement de contenu (CDM).</span><span class="sxs-lookup"><span data-stu-id="33bc4-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="33bc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33bc4-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="33bc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33bc4-106">Parameters</span></span>

<span data-ttu-id="33bc4-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="33bc4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33bc4-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33bc4-108">Return value</span></span>

<span data-ttu-id="33bc4-109">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33bc4-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33bc4-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33bc4-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33bc4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33bc4-111">Requirements</span></span>



| <span data-ttu-id="33bc4-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33bc4-112">Requirement</span></span> | <span data-ttu-id="33bc4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="33bc4-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bc4-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33bc4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="33bc4-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33bc4-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33bc4-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33bc4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="33bc4-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33bc4-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="33bc4-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="33bc4-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33bc4-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33bc4-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bc4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33bc4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bc4-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="33bc4-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




