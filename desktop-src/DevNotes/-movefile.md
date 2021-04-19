---
description: Déplace un fichier ou un répertoire existant, y compris ses enfants.
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: _MoveFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532736"
---
# <a name="_movefile-function"></a><span data-ttu-id="ce438-103">\_MoveFile, fonction</span><span class="sxs-lookup"><span data-stu-id="ce438-103">\_MoveFile function</span></span>

<span data-ttu-id="ce438-104">\[Cette fonction est un wrapper sur la fonction **MoveFile** .</span><span class="sxs-lookup"><span data-stu-id="ce438-104">\[This function is a wrapper over the **MoveFile** function.</span></span> <span data-ttu-id="ce438-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ce438-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ce438-106">Les applications doivent appeler **MoveFile** directement.\]</span><span class="sxs-lookup"><span data-stu-id="ce438-106">Applications should call **MoveFile** directly.\]</span></span>

<span data-ttu-id="ce438-107">Déplace un fichier ou un répertoire existant, y compris ses enfants.</span><span class="sxs-lookup"><span data-stu-id="ce438-107">Moves an existing file or directory, including its children.</span></span> <span data-ttu-id="ce438-108">Voir [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span><span class="sxs-lookup"><span data-stu-id="ce438-108">See [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce438-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce438-109">Syntax</span></span>


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ce438-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce438-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce438-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ce438-111">*...*</span></span> 
<span data-ttu-id="ce438-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ce438-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ce438-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce438-113">Requirements</span></span>



| <span data-ttu-id="ce438-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce438-114">Requirement</span></span> | <span data-ttu-id="ce438-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce438-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce438-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ce438-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ce438-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce438-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce438-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce438-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce438-119">**MoveFile**</span><span class="sxs-lookup"><span data-stu-id="ce438-119">**MoveFile**</span></span>](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
