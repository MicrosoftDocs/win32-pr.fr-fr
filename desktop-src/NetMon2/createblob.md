---
description: La fonction CreateBlob crée un objet BLOB vide.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: CreateBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756886"
---
# <a name="createblob-function"></a><span data-ttu-id="8b2dd-103">CreateBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="8b2dd-103">CreateBlob function</span></span>

<span data-ttu-id="8b2dd-104">La fonction **CreateBlob** crée un objet BLOB vide.</span><span class="sxs-lookup"><span data-stu-id="8b2dd-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b2dd-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8b2dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b2dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2dd-107">*phBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8b2dd-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2dd-108">Pointeur vers la variable où le pointeur vers le nouvel objet BLOB est retourné.</span><span class="sxs-lookup"><span data-stu-id="8b2dd-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2dd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b2dd-109">Return value</span></span>

<span data-ttu-id="8b2dd-110">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8b2dd-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8b2dd-111">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8b2dd-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2dd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b2dd-112">Requirements</span></span>



| <span data-ttu-id="8b2dd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b2dd-113">Requirement</span></span> | <span data-ttu-id="8b2dd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b2dd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2dd-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b2dd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2dd-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b2dd-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b2dd-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b2dd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2dd-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b2dd-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b2dd-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b2dd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b2dd-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b2dd-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="8b2dd-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b2dd-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b2dd-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b2dd-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b2dd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2dd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b2dd-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2dd-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b2dd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b2dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2dd-126">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="8b2dd-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




