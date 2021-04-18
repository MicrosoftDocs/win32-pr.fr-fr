---
title: IMsRdpDriveCollection propriété DriveCount
description: Récupère le nombre d’objets dans la collection. | IMsRdpDriveCollection propriété DriveCount
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveCount
- Services Bureau à distance de la propriété DriveCount, interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, propriété DriveCount
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523161"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="b7462-107">IMsRdpDriveCollection ::D propriété riveCount</span><span class="sxs-lookup"><span data-stu-id="b7462-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="b7462-108">Récupère le nombre d’objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b7462-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="b7462-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7462-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7462-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7462-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="b7462-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b7462-111">Property value</span></span>

<span data-ttu-id="b7462-112">Nombre d’objets.</span><span class="sxs-lookup"><span data-stu-id="b7462-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7462-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b7462-113">Error codes</span></span>

<span data-ttu-id="b7462-114">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="b7462-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="b7462-115">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="b7462-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7462-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7462-116">Requirements</span></span>



| <span data-ttu-id="b7462-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7462-117">Requirement</span></span> | <span data-ttu-id="b7462-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7462-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7462-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7462-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7462-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7462-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b7462-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7462-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7462-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7462-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b7462-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b7462-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7462-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7462-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b7462-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7462-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7462-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7462-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b7462-127">IID</span><span class="sxs-lookup"><span data-stu-id="b7462-127">IID</span></span><br/>                      | <span data-ttu-id="b7462-128">IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="b7462-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7462-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7462-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7462-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="b7462-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





