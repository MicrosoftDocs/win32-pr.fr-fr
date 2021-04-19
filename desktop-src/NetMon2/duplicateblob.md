---
description: La fonction DuplicateBlob copie un objet BLOB spécifique.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: DuplicateBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540884"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="c1024-103">DuplicateBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="c1024-103">DuplicateBlob function</span></span>

<span data-ttu-id="c1024-104">La fonction **DuplicateBlob** copie un objet BLOB spécifique.</span><span class="sxs-lookup"><span data-stu-id="c1024-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1024-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1024-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="c1024-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1024-107">*hSrcBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1024-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1024-108">Handle de l’objet BLOB copié.</span><span class="sxs-lookup"><span data-stu-id="c1024-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="c1024-109">*hBlobThatWillBeCreated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c1024-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1024-110">Handle vers l’objet BLOB dupliqué.</span><span class="sxs-lookup"><span data-stu-id="c1024-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1024-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1024-111">Return value</span></span>

<span data-ttu-id="c1024-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c1024-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c1024-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c1024-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1024-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1024-114">Requirements</span></span>



| <span data-ttu-id="c1024-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1024-115">Requirement</span></span> | <span data-ttu-id="c1024-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1024-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1024-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1024-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c1024-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1024-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c1024-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1024-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c1024-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1024-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1024-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1024-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1024-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1024-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c1024-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1024-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1024-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1024-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1024-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c1024-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1024-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1024-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1024-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1024-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1024-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="c1024-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="c1024-129">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="c1024-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




