---
description: Recherche le frame suivant dans le contexte de capture actuel qui correspond au filtre.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: FindNextFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525150"
---
# <a name="findnextframe-function"></a><span data-ttu-id="fad35-103">FindNextFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="fad35-103">FindNextFrame function</span></span>

<span data-ttu-id="fad35-104">La fonction **FindNextFrame** recherche le frame suivant dans le contexte de capture actuel qui correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="fad35-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fad35-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="fad35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fad35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad35-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="fad35-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-108">Handle du frame.</span><span class="sxs-lookup"><span data-stu-id="fad35-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="fad35-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="fad35-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-110">Nom de protocole, tel que TCP.</span><span class="sxs-lookup"><span data-stu-id="fad35-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="fad35-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="fad35-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-112">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="fad35-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="fad35-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="fad35-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-114">Adresse source.</span><span class="sxs-lookup"><span data-stu-id="fad35-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="fad35-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="fad35-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-116">Pointeur vers un **mot** qui recevra le décalage de protocole.</span><span class="sxs-lookup"><span data-stu-id="fad35-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="fad35-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="fad35-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-118">Point de départ de la recherche.</span><span class="sxs-lookup"><span data-stu-id="fad35-118">The starting point of the search.</span></span> <span data-ttu-id="fad35-119">Par défaut, cette fonction recherche les frames Forward 1 000 à partir du point de départ *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="fad35-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="fad35-120">Pour modifier la distance de recherche, ajoutez la ligne suivante au fichier Nmapi.ini, situé dans le \\ répertoire Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="fad35-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="fad35-121">MAXLOOKBACK =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="fad35-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="fad35-122">*HighestFrame*</span><span class="sxs-lookup"><span data-stu-id="fad35-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="fad35-123">Numéro de trame le plus élevé dans la capture dans laquelle la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="fad35-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad35-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fad35-124">Return value</span></span>

<span data-ttu-id="fad35-125">Si la fonction réussit, la valeur de retour est un handle vers le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="fad35-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="fad35-126">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="fad35-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad35-127">Notes</span><span class="sxs-lookup"><span data-stu-id="fad35-127">Remarks</span></span>

<span data-ttu-id="fad35-128">Le filtre de capture est défini principalement par le paramètre *ProtocolName* , qui est la seule entrée de filtre requise ; vous pouvez ajouter des données *DestinationAddress* et *sourceAddress* pour augmenter la vitesse de capture.</span><span class="sxs-lookup"><span data-stu-id="fad35-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="fad35-129">Le pointeur *ProtocolOffset* est retourné à l’analyseur appelant, qui ajoute le **mot** au pointeur retourné en verrouillant le frame (avec [ParserTemporaryLockFrame](parsertemporarylockframe.md)) pour obtenir le **LPBYTE** du protocole recherché.</span><span class="sxs-lookup"><span data-stu-id="fad35-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="fad35-130">Au retour, le HFRAME qui a réussi le filtre est donné à l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="fad35-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="fad35-131">Si l’analyseur constate que ce frame n’est pas celui qui est recherché, l’analyseur peut remettre le HFRAME à la fonction **FindNextFrame** pour accéder au frame suivant.</span><span class="sxs-lookup"><span data-stu-id="fad35-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="fad35-132">Les adresses source et de destination ne sont pas requises et peuvent être passées comme **null**.</span><span class="sxs-lookup"><span data-stu-id="fad35-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad35-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fad35-133">Requirements</span></span>



| <span data-ttu-id="fad35-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fad35-134">Requirement</span></span> | <span data-ttu-id="fad35-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad35-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fad35-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fad35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fad35-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fad35-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fad35-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fad35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fad35-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fad35-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fad35-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="fad35-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad35-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad35-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fad35-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fad35-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="fad35-143"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fad35-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fad35-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fad35-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fad35-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad35-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




