---
description: La fonction DeleteExtractedFiles supprime les fichiers qui ont été extraits par la fonction Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526062"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="c4107-103">DeleteExtractedFiles fonction)</span><span class="sxs-lookup"><span data-stu-id="c4107-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="c4107-104">\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]</span><span class="sxs-lookup"><span data-stu-id="c4107-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="c4107-105">La fonction **DeleteExtractedFiles** supprime les fichiers qui ont été extraits par la fonction [**extract**](extract.md) .</span><span class="sxs-lookup"><span data-stu-id="c4107-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4107-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4107-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="c4107-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4107-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4107-108">*alimentation*</span><span class="sxs-lookup"><span data-stu-id="c4107-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="c4107-109">Pointeur vers une structure de [**session**](session.md) qui contient des informations sur la session active.</span><span class="sxs-lookup"><span data-stu-id="c4107-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="c4107-110">Cette fonction libère la mémoire dans le membre **pFileList** de cette structure et affecte à **PFileList** la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c4107-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4107-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4107-111">Return value</span></span>

<span data-ttu-id="c4107-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c4107-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4107-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c4107-113">Remarks</span></span>

<span data-ttu-id="c4107-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c4107-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4107-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4107-115">Requirements</span></span>



| <span data-ttu-id="c4107-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4107-116">Requirement</span></span> | <span data-ttu-id="c4107-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4107-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4107-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c4107-118">DLL</span></span><br/> | <dl> <span data-ttu-id="c4107-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4107-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4107-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4107-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4107-121">**Extraction**</span><span class="sxs-lookup"><span data-stu-id="c4107-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="c4107-122">**SESSION**</span><span class="sxs-lookup"><span data-stu-id="c4107-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
