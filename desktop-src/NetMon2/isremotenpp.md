---
description: La fonction IsRemoteNPP indique si l’objet BLOB donné spécifie un NPP distant.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: IsRemoteNPP, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755389"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="82157-103">IsRemoteNPP fonction)</span><span class="sxs-lookup"><span data-stu-id="82157-103">IsRemoteNPP function</span></span>

<span data-ttu-id="82157-104">La fonction **IsRemoteNPP** indique si l’objet BLOB donné spécifie un NPP distant.</span><span class="sxs-lookup"><span data-stu-id="82157-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="82157-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82157-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="82157-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82157-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82157-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82157-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82157-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="82157-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82157-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82157-109">Return value</span></span>

<span data-ttu-id="82157-110">Si la fonction réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="82157-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="82157-111">Notes</span><span class="sxs-lookup"><span data-stu-id="82157-111">Remarks</span></span>

<span data-ttu-id="82157-112">Utilisez cette fonction pour tester si une catégorie distante existe.</span><span class="sxs-lookup"><span data-stu-id="82157-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="82157-113">Assurez-vous que les noms des ordinateurs locaux et distants sont différents.</span><span class="sxs-lookup"><span data-stu-id="82157-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="82157-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82157-114">Requirements</span></span>



| <span data-ttu-id="82157-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82157-115">Requirement</span></span> | <span data-ttu-id="82157-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="82157-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82157-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82157-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82157-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82157-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="82157-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82157-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82157-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82157-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82157-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="82157-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="82157-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82157-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="82157-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82157-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="82157-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82157-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="82157-125">DLL</span><span class="sxs-lookup"><span data-stu-id="82157-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82157-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82157-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




