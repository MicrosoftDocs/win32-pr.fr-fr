---
description: La fonction MergeBlob copie toutes les entrées de l’objet BLOB source dans un objet BLOB de destination.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: MergeBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951268"
---
# <a name="mergeblob-function"></a><span data-ttu-id="13bb0-103">MergeBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="13bb0-103">MergeBlob function</span></span>

<span data-ttu-id="13bb0-104">La fonction **MergeBlob** copie toutes les entrées de l’objet BLOB source dans un objet blob de destination.</span><span class="sxs-lookup"><span data-stu-id="13bb0-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bb0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13bb0-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="13bb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13bb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bb0-107">*hDstBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13bb0-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13bb0-108">Handle vers l’objet BLOB de destination.</span><span class="sxs-lookup"><span data-stu-id="13bb0-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="13bb0-109">En entrée, cet objet BLOB contient ses informations d’origine.</span><span class="sxs-lookup"><span data-stu-id="13bb0-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="13bb0-110">En sortie, cet objet BLOB contient ses informations d’origine, ainsi que toutes les informations de l’objet BLOB source.</span><span class="sxs-lookup"><span data-stu-id="13bb0-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="13bb0-111">*hSrcBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13bb0-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13bb0-112">Handle de l’objet BLOB source.</span><span class="sxs-lookup"><span data-stu-id="13bb0-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bb0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13bb0-113">Return value</span></span>

<span data-ttu-id="13bb0-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="13bb0-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="13bb0-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="13bb0-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bb0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="13bb0-116">Remarks</span></span>

<span data-ttu-id="13bb0-117">Les entrées communes aux fichiers source et de destination seront remplacées par les données de l’objet BLOB source.</span><span class="sxs-lookup"><span data-stu-id="13bb0-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bb0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13bb0-118">Requirements</span></span>



| <span data-ttu-id="13bb0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13bb0-119">Requirement</span></span> | <span data-ttu-id="13bb0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="13bb0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13bb0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13bb0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13bb0-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13bb0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13bb0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13bb0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13bb0-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13bb0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13bb0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="13bb0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13bb0-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="13bb0-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="13bb0-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="13bb0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="13bb0-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13bb0-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="13bb0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="13bb0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13bb0-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bb0-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




