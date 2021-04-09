---
title: Message MMIOM_WRITE (mmsystem. h)
description: Le \_ message d’écriture MMIOM est envoyé à une procédure d’e/s par la fonction mmioWrite pour demander l’écriture des données dans un fichier ouvert.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- Message MMIOM_WRITE Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942745"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="ae82d-104">MMIOM \_ écrire un message</span><span class="sxs-lookup"><span data-stu-id="ae82d-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="ae82d-105">Le message d' **\_ écriture MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) pour demander l’écriture des données dans un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="ae82d-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="ae82d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae82d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae82d-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="ae82d-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="ae82d-108">Pointeur vers une mémoire tampon contenant les données à écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ae82d-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="ae82d-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="ae82d-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="ae82d-110">Nombre d’octets à écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ae82d-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae82d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae82d-111">Return Value</span></span>

<span data-ttu-id="ae82d-112">Retourne le nombre d’octets réellement écrits dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ae82d-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="ae82d-113">En cas d’erreur, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="ae82d-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae82d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ae82d-114">Remarks</span></span>

<span data-ttu-id="ae82d-115">La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ae82d-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae82d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae82d-116">Requirements</span></span>



| <span data-ttu-id="ae82d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae82d-117">Requirement</span></span> | <span data-ttu-id="ae82d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae82d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae82d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae82d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae82d-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae82d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae82d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae82d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae82d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae82d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ae82d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae82d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae82d-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae82d-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

