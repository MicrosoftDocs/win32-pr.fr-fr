---
title: Méthode IMsRdpDriveCollection RescanDrives
description: Actualise la liste des objets dans la collection. | Méthode IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RescanDrives
- Méthode RescanDrives Services Bureau à distance, interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, méthode RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538281"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="9c8e3-107">IMsRdpDriveCollection :: RescanDrives, méthode</span><span class="sxs-lookup"><span data-stu-id="9c8e3-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="9c8e3-108">Actualise la liste des objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9c8e3-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c8e3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c8e3-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="9c8e3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c8e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8e3-111">*vboolDynRedir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c8e3-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c8e3-112">État de redirection par défaut qui sera appliqué aux périphériques ou lecteurs récemment découverts.</span><span class="sxs-lookup"><span data-stu-id="9c8e3-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c8e3-113">Return value</span></span>

<span data-ttu-id="9c8e3-114">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="9c8e3-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="9c8e3-115">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="9c8e3-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8e3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c8e3-116">Requirements</span></span>



| <span data-ttu-id="9c8e3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c8e3-117">Requirement</span></span> | <span data-ttu-id="9c8e3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c8e3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8e3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8e3-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c8e3-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9c8e3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8e3-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c8e3-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9c8e3-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9c8e3-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c8e3-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c8e3-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="9c8e3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9c8e3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c8e3-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c8e3-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="9c8e3-127">IID</span><span class="sxs-lookup"><span data-stu-id="9c8e3-127">IID</span></span><br/>                      | <span data-ttu-id="9c8e3-128">IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="9c8e3-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c8e3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c8e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8e3-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="9c8e3-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





