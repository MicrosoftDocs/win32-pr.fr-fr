---
title: Message MMIOM_READ (mmsystem. h)
description: Le \_ message de lecture MMIOM est envoyé à une procédure d’e/s par la fonction mmioRead pour demander qu’un nombre spécifié d’octets soit lu à partir d’un fichier ouvert.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- Message MMIOM_READ Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467079"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="e5c99-104">MMIOM \_ lire le message</span><span class="sxs-lookup"><span data-stu-id="e5c99-104">MMIOM\_READ message</span></span>

<span data-ttu-id="e5c99-105">Le message de **\_ lecture MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) pour demander qu’un nombre spécifié d’octets soit lu à partir d’un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="e5c99-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="e5c99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c99-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span><span class="sxs-lookup"><span data-stu-id="e5c99-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="e5c99-108">Pointeur vers la mémoire tampon à remplir avec les données lues à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="e5c99-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="e5c99-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span><span class="sxs-lookup"><span data-stu-id="e5c99-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="e5c99-110">Nombre d’octets à lire à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="e5c99-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c99-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5c99-111">Return Value</span></span>

<span data-ttu-id="e5c99-112">Retourne le nombre d’octets réellement lus à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="e5c99-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="e5c99-113">Si le nombre d’octets ne peut pas être lu, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="e5c99-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="e5c99-114">En cas d’erreur, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="e5c99-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c99-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e5c99-115">Remarks</span></span>

<span data-ttu-id="e5c99-116">La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="e5c99-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c99-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c99-117">Requirements</span></span>



| <span data-ttu-id="e5c99-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5c99-118">Requirement</span></span> | <span data-ttu-id="e5c99-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5c99-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c99-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c99-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5c99-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5c99-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c99-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5c99-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5c99-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5c99-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c99-125"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c99-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

