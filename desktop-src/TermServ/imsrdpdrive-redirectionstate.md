---
title: IMsRdpDrive propriété RedirectionState
description: Indique l’état de redirection du lecteur.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectionState
- Services Bureau à distance de la propriété RedirectionState, interface IMsRdpDrive
- Services Bureau à distance de l’interface IMsRdpDrive, propriété RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384984"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="6870f-106">IMsRdpDrive :: RedirectionState, propriété</span><span class="sxs-lookup"><span data-stu-id="6870f-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="6870f-107">Indique l’état de redirection du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6870f-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="6870f-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6870f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6870f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6870f-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="6870f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6870f-110">Property value</span></span>

<span data-ttu-id="6870f-111">Affectez à ce paramètre la valeur **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="6870f-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="6870f-112">pour désactiver la redirection ou la **variante \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6870f-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="6870f-113">pour activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="6870f-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6870f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6870f-114">Error codes</span></span>

<span data-ttu-id="6870f-115">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="6870f-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="6870f-116">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="6870f-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6870f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6870f-117">Requirements</span></span>



| <span data-ttu-id="6870f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6870f-118">Requirement</span></span> | <span data-ttu-id="6870f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6870f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6870f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6870f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6870f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6870f-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6870f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6870f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6870f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6870f-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6870f-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6870f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6870f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6870f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6870f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6870f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6870f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6870f-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6870f-128">IID</span><span class="sxs-lookup"><span data-stu-id="6870f-128">IID</span></span><br/>                      | <span data-ttu-id="6870f-129">IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="6870f-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="6870f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6870f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6870f-131">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="6870f-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





