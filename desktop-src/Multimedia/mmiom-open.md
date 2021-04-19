---
title: Message MMIOM_OPEN (mmsystem. h)
description: Le \_ message MMIOM Open est envoyé à une procédure d’e/s par la fonction mmioOpen pour demander l’ouverture ou la suppression d’un fichier.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- Message MMIOM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538818"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="daa15-104">MMIOM \_ ouvrir le message</span><span class="sxs-lookup"><span data-stu-id="daa15-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="daa15-105">Le message **MMIOM \_ Open** est envoyé à une procédure d’e/s par la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) pour demander l’ouverture ou la suppression d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="daa15-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="daa15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daa15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa15-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span><span class="sxs-lookup"><span data-stu-id="daa15-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="daa15-108">Chaîne terminée par le caractère null qui contient le nom du fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="daa15-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="daa15-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="daa15-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="daa15-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="daa15-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa15-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="daa15-111">Return Value</span></span>

<span data-ttu-id="daa15-112">Retourne MMSYSERR \_ NOerreur en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="daa15-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="daa15-113">Les valeurs d’erreur possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="daa15-113">Possible error values include the following:</span></span>



| <span data-ttu-id="daa15-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daa15-114">Requirement</span></span> | <span data-ttu-id="daa15-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="daa15-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="daa15-116">MMIOM \_ CANNOTOPEN</span><span class="sxs-lookup"><span data-stu-id="daa15-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="daa15-117">Impossible d’ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="daa15-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="daa15-118">MMIOM \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="daa15-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="daa15-119">Mémoire insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="daa15-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="daa15-120">Notes</span><span class="sxs-lookup"><span data-stu-id="daa15-120">Remarks</span></span>

<span data-ttu-id="daa15-121">Le membre **dwFlags** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contient des indicateurs passés à la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="daa15-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="daa15-122">Le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) est initialisé à zéro.</span><span class="sxs-lookup"><span data-stu-id="daa15-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="daa15-123">Si cette valeur est incorrecte, la procédure d’e/s doit la corriger.</span><span class="sxs-lookup"><span data-stu-id="daa15-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="daa15-124">Si l’application a passé une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) à [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), la valeur de retour est retournée dans le membre **wErrorRet** .</span><span class="sxs-lookup"><span data-stu-id="daa15-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="daa15-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daa15-125">Requirements</span></span>



| <span data-ttu-id="daa15-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daa15-126">Requirement</span></span> | <span data-ttu-id="daa15-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="daa15-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa15-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa15-128">Minimum supported client</span></span><br/> | <span data-ttu-id="daa15-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daa15-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="daa15-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa15-130">Minimum supported server</span></span><br/> | <span data-ttu-id="daa15-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daa15-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="daa15-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="daa15-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="daa15-133"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daa15-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

