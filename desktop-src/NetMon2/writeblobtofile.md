---
description: La fonction WriteBlobToFile écrit un objet BLOB dans un fichier.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: WriteBlobToFile, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526174"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="a8c26-103">WriteBlobToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="a8c26-103">WriteBlobToFile function</span></span>

<span data-ttu-id="a8c26-104">La fonction **WriteBlobToFile** écrit un objet BLOB dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c26-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8c26-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="a8c26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c26-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8c26-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c26-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="a8c26-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a8c26-109">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8c26-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c26-110">Pointeur vers le nom du fichier dans lequel l’objet BLOB est enregistré.</span><span class="sxs-lookup"><span data-stu-id="a8c26-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c26-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8c26-111">Return value</span></span>

<span data-ttu-id="a8c26-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a8c26-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a8c26-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a8c26-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c26-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8c26-114">Requirements</span></span>



| <span data-ttu-id="a8c26-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8c26-115">Requirement</span></span> | <span data-ttu-id="a8c26-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8c26-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c26-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8c26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c26-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8c26-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a8c26-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8c26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c26-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8c26-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8c26-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8c26-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c26-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c26-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a8c26-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8c26-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8c26-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8c26-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8c26-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c26-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c26-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c26-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




