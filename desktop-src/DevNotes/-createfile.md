---
description: Crée ou ouvre un fichier.
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: _CreateFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523962"
---
# <a name="_createfile-function"></a><span data-ttu-id="25e58-103">\_CreateFile, fonction</span><span class="sxs-lookup"><span data-stu-id="25e58-103">\_CreateFile function</span></span>

<span data-ttu-id="25e58-104">\[Cette fonction est un wrapper sur la fonction **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="25e58-104">\[This function is a wrapper over the **CreateFile** function.</span></span> <span data-ttu-id="25e58-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="25e58-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="25e58-106">Les applications doivent appeler **CreateFile** directement.\]</span><span class="sxs-lookup"><span data-stu-id="25e58-106">Applications should call **CreateFile** directly.\]</span></span>

<span data-ttu-id="25e58-107">Crée ou ouvre un fichier.</span><span class="sxs-lookup"><span data-stu-id="25e58-107">Creates or opens a file.</span></span> <span data-ttu-id="25e58-108">Consultez [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="25e58-108">See [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span></span>

## <a name="syntax"></a><span data-ttu-id="25e58-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25e58-109">Syntax</span></span>


```C++
BOOL _CreateFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="25e58-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25e58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25e58-111">*...*</span><span class="sxs-lookup"><span data-stu-id="25e58-111">*...*</span></span> 
<span data-ttu-id="25e58-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="25e58-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="25e58-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25e58-113">Requirements</span></span>



| <span data-ttu-id="25e58-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25e58-114">Requirement</span></span> | <span data-ttu-id="25e58-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="25e58-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e58-116">DLL</span><span class="sxs-lookup"><span data-stu-id="25e58-116">DLL</span></span><br/> | <dl> <span data-ttu-id="25e58-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25e58-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e58-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25e58-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e58-119">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="25e58-119">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

