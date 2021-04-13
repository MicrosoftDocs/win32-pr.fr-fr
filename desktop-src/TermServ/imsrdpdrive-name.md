---
title: Propriété IMsRdpDrive Name
description: Récupère le nom du lecteur.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Propriété Name Services Bureau à distance
- Name, propriété Services Bureau à distance, IMsRdpDrive, interface
- Services Bureau à distance de l’interface IMsRdpDrive, propriété Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465990"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="5ed0a-106">IMsRdpDrive :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="5ed0a-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="5ed0a-107">Récupère le nom du lecteur.</span><span class="sxs-lookup"><span data-stu-id="5ed0a-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="5ed0a-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5ed0a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed0a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ed0a-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="5ed0a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5ed0a-110">Property value</span></span>

<span data-ttu-id="5ed0a-111">Nom du lecteur.</span><span class="sxs-lookup"><span data-stu-id="5ed0a-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ed0a-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5ed0a-112">Error codes</span></span>

<span data-ttu-id="5ed0a-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="5ed0a-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="5ed0a-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="5ed0a-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed0a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ed0a-115">Requirements</span></span>



| <span data-ttu-id="5ed0a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ed0a-116">Requirement</span></span> | <span data-ttu-id="5ed0a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ed0a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed0a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ed0a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed0a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ed0a-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5ed0a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ed0a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed0a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ed0a-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5ed0a-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5ed0a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ed0a-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0a-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ed0a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed0a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed0a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ed0a-126">IID</span><span class="sxs-lookup"><span data-stu-id="5ed0a-126">IID</span></span><br/>                      | <span data-ttu-id="5ed0a-127">IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="5ed0a-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5ed0a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ed0a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed0a-129">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="5ed0a-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





