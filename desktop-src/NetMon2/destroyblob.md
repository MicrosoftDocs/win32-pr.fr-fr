---
description: La fonction DestroyBlob libère toute la mémoire associée à l’objet BLOB, puis détruit l’objet BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: DestroyBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524448"
---
# <a name="destroyblob-function"></a><span data-ttu-id="e9f1f-103">DestroyBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="e9f1f-103">DestroyBlob function</span></span>

<span data-ttu-id="e9f1f-104">La fonction **DestroyBlob** libère toute la mémoire associée à l’objet BLOB, puis détruit l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e9f1f-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9f1f-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="e9f1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9f1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f1f-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9f1f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f1f-108">Handle vers l’objet BLOB qui est détruit.</span><span class="sxs-lookup"><span data-stu-id="e9f1f-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f1f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9f1f-109">Return value</span></span>

<span data-ttu-id="e9f1f-110">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e9f1f-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e9f1f-111">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9f1f-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f1f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f1f-112">Requirements</span></span>



| <span data-ttu-id="e9f1f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f1f-113">Requirement</span></span> | <span data-ttu-id="e9f1f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f1f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f1f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f1f-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f1f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9f1f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f1f-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f1f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9f1f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f1f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f1f-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f1f-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e9f1f-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9f1f-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9f1f-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f1f-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9f1f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f1f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f1f-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9f1f-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f1f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f1f-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="e9f1f-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 




