---
title: Message MMIOM_RENAME (mmsystem. h)
description: Le \_ message MMIOM Rename est envoyé à une procédure d’e/s par la fonction mmioRename pour demander que le fichier spécifié soit renommé.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- Message MMIOM_RENAME Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466467"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="85b19-104">MMIOM \_ REnommer le message</span><span class="sxs-lookup"><span data-stu-id="85b19-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="85b19-105">Le message **MMIOM \_ Rename** est envoyé à une procédure d’e/s par la fonction [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) pour demander que le fichier spécifié soit renommé.</span><span class="sxs-lookup"><span data-stu-id="85b19-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="85b19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b19-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span><span class="sxs-lookup"><span data-stu-id="85b19-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="85b19-108">Pointeur vers une chaîne contenant le nom du fichier à renommer.</span><span class="sxs-lookup"><span data-stu-id="85b19-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="85b19-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span><span class="sxs-lookup"><span data-stu-id="85b19-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="85b19-110">Pointeur vers une chaîne contenant le nouveau nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="85b19-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b19-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85b19-111">Return Value</span></span>

<span data-ttu-id="85b19-112">Si le fichier est correctement renommé, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="85b19-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="85b19-113">Si le fichier spécifié est introuvable, la valeur de retour est MMIOERR \_ FILENOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="85b19-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b19-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85b19-114">Requirements</span></span>



| <span data-ttu-id="85b19-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85b19-115">Requirement</span></span> | <span data-ttu-id="85b19-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="85b19-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b19-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85b19-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85b19-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85b19-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85b19-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85b19-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85b19-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85b19-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85b19-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="85b19-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85b19-122"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85b19-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

