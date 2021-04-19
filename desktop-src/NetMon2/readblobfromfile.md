---
description: La fonction ReadBlobFromFile lit un objet BLOB dans un fichier.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: ReadBlobFromFile, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545158"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="58a87-103">ReadBlobFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="58a87-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="58a87-104">La fonction **ReadBlobFromFile** lit un objet BLOB dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="58a87-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a87-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="58a87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58a87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a87-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58a87-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a87-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="58a87-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="58a87-109">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58a87-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a87-110">Pointeur vers le nom du fichier qui contient l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="58a87-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a87-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58a87-111">Return value</span></span>

<span data-ttu-id="58a87-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="58a87-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="58a87-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="58a87-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a87-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58a87-114">Requirements</span></span>



| <span data-ttu-id="58a87-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58a87-115">Requirement</span></span> | <span data-ttu-id="58a87-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a87-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58a87-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a87-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58a87-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a87-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58a87-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a87-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58a87-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a87-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58a87-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="58a87-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a87-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="58a87-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="58a87-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58a87-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="58a87-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58a87-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="58a87-125">DLL</span><span class="sxs-lookup"><span data-stu-id="58a87-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58a87-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a87-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




