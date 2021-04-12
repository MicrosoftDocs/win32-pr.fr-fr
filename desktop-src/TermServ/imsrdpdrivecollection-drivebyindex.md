---
title: IMsRdpDriveCollection propriété DriveByIndex
description: Récupère le lecteur à l’index spécifié.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveByIndex
- Services Bureau à distance de la propriété DriveByIndex, interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, propriété DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384983"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="4de14-106">IMsRdpDriveCollection ::D propriété riveByIndex</span><span class="sxs-lookup"><span data-stu-id="4de14-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="4de14-107">Récupère le lecteur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="4de14-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="4de14-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4de14-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4de14-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="4de14-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4de14-110">Property value</span></span>

<span data-ttu-id="4de14-111">Pointeur d’interface [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="4de14-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4de14-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4de14-112">Error codes</span></span>

<span data-ttu-id="4de14-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="4de14-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="4de14-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="4de14-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de14-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4de14-115">Requirements</span></span>



| <span data-ttu-id="4de14-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4de14-116">Requirement</span></span> | <span data-ttu-id="4de14-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4de14-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de14-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4de14-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de14-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4de14-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4de14-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4de14-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4de14-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4de14-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4de14-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de14-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4de14-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4de14-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de14-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de14-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4de14-126">IID</span><span class="sxs-lookup"><span data-stu-id="4de14-126">IID</span></span><br/>                      | <span data-ttu-id="4de14-127">IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="4de14-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4de14-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4de14-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de14-129">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="4de14-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





