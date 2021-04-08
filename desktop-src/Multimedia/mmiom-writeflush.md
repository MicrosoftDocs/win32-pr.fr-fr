---
title: Message MMIOM_WRITEFLUSH (mmsystem. h)
description: Le \_ message MMIOM WRITEFLUSH est envoyé à une procédure d’e/s par la fonction mmioWrite pour demander que les données soient écrites dans un fichier ouvert et que les mémoires tampons internes utilisées par la procédure d’e/s soient vidées sur le disque.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- Message MMIOM_WRITEFLUSH Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743357"
---
# <a name="mmiom_writeflush-message"></a><span data-ttu-id="46316-104">\_Message MMIOM WRITEFLUSH</span><span class="sxs-lookup"><span data-stu-id="46316-104">MMIOM\_WRITEFLUSH message</span></span>

<span data-ttu-id="46316-105">Le message **MMIOM \_ WRITEFLUSH** est envoyé à une procédure d’e/s par la fonction [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) pour demander que les données soient écrites dans un fichier ouvert et que les mémoires tampons internes utilisées par la procédure d’e/s soient vidées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="46316-105">The **MMIOM\_WRITEFLUSH** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file and that any internal buffers used by the I/O procedure be flushed to disk.</span></span>


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="46316-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46316-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="46316-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="46316-108">Pointeur vers une mémoire tampon contenant les données à écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="46316-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="46316-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="46316-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="46316-110">Nombre d’octets à écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="46316-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46316-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="46316-111">Return Value</span></span>

<span data-ttu-id="46316-112">Retourne le nombre d’octets réellement écrits dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="46316-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="46316-113">En cas d’erreur, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="46316-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="46316-114">Notes</span><span class="sxs-lookup"><span data-stu-id="46316-114">Remarks</span></span>

<span data-ttu-id="46316-115">La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="46316-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

<span data-ttu-id="46316-116">Ce message est équivalent au message [**d' \_ écriture MMIOM**](mmiom-write.md) , à ceci près qu’il demande que la procédure d’e/s vide ses mémoires tampons internes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="46316-116">This message is equivalent to the [**MMIOM\_WRITE**](mmiom-write.md) message except that it requests that the I/O procedure flush its internal buffers, if any.</span></span> <span data-ttu-id="46316-117">À moins qu’une procédure d’e/s effectue une mise en mémoire tampon interne, ce message peut être géré exactement comme le message d' **\_ écriture MMIOM** .</span><span class="sxs-lookup"><span data-stu-id="46316-117">Unless an I/O procedure performs internal buffering, this message can be handled exactly like the **MMIOM\_WRITE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="46316-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46316-118">Requirements</span></span>



| <span data-ttu-id="46316-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46316-119">Requirement</span></span> | <span data-ttu-id="46316-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="46316-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46316-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46316-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46316-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46316-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46316-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46316-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46316-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46316-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46316-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="46316-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="46316-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46316-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

