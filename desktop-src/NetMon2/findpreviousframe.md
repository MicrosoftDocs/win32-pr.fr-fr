---
description: La fonction FindPreviousFrame recherche le frame précédent dans le contexte de capture actuel qui correspond au filtre.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: FindPreviousFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950973"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="b504a-103">FindPreviousFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="b504a-103">FindPreviousFrame function</span></span>

<span data-ttu-id="b504a-104">La fonction **FindPreviousFrame** recherche le frame précédent dans le contexte de capture actuel qui correspond au filtre.</span><span class="sxs-lookup"><span data-stu-id="b504a-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b504a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b504a-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b504a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b504a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b504a-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="b504a-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="b504a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b504a-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="b504a-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-110">Nom de protocole, tel que TCP.</span><span class="sxs-lookup"><span data-stu-id="b504a-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="b504a-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="b504a-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-112">Adresse de destination du frame recherché.</span><span class="sxs-lookup"><span data-stu-id="b504a-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="b504a-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="b504a-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-114">Adresse source du frame recherché.</span><span class="sxs-lookup"><span data-stu-id="b504a-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="b504a-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="b504a-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-116">Pointeur vers un **mot** qui reçoit le décalage de protocole.</span><span class="sxs-lookup"><span data-stu-id="b504a-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="b504a-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="b504a-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-118">Point de départ de la recherche.</span><span class="sxs-lookup"><span data-stu-id="b504a-118">Starting point of the search.</span></span> <span data-ttu-id="b504a-119">Par défaut, cette fonction effectue une recherche vers l’arrière 1 000 frames à partir du point de départ *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="b504a-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="b504a-120">Vous pouvez modifier la distance de recherche en ajoutant cette ligne au fichier Nmapi.ini, qui se trouve dans le \\ répertoire Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="b504a-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="b504a-121">MAXLOOKBACK =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="b504a-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="b504a-122">*LowestFrame*</span><span class="sxs-lookup"><span data-stu-id="b504a-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b504a-123">Numéro de trame le plus bas dans la capture dans laquelle la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="b504a-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b504a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b504a-124">Return value</span></span>

<span data-ttu-id="b504a-125">Si la fonction réussit, la valeur de retour est un handle vers le frame précédent.</span><span class="sxs-lookup"><span data-stu-id="b504a-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="b504a-126">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="b504a-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b504a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b504a-127">Remarks</span></span>

<span data-ttu-id="b504a-128">Le filtre de capture est défini principalement par *ProtocolName*, qui est la seule entrée de filtre requise ; vous pouvez ajouter des informations *DestinationAddress* et *sourceAddress* pour augmenter la vitesse de capture.</span><span class="sxs-lookup"><span data-stu-id="b504a-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="b504a-129">*ProtocolOffset* est retourné à l’analyseur appelant, ce qui ajoute ce **DWORD** au pointeur retourné par le verrouillage du frame (avec [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) pour obtenir le LPBYTE du protocole recherché.</span><span class="sxs-lookup"><span data-stu-id="b504a-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="b504a-130">Au retour, le HFRAME qui a réussi le filtre est donné à l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="b504a-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="b504a-131">Si l’analyseur constate que le frame n’est pas celui qui est recherché, l’analyseur peut remettre ce HFRAME à la fonction **FindPreviousFrame** pour récupérer le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="b504a-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="b504a-132">Les adresses source et de destination, qui ne sont pas nécessaires, peuvent être transmises en tant que **valeurs NULL**.</span><span class="sxs-lookup"><span data-stu-id="b504a-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="b504a-133">En cas d’utilisation, ces adresses peuvent être de type adresse \_ \_ IP, et ainsi de suite, pas seulement des types Mac.</span><span class="sxs-lookup"><span data-stu-id="b504a-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="b504a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b504a-134">Requirements</span></span>



| <span data-ttu-id="b504a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b504a-135">Requirement</span></span> | <span data-ttu-id="b504a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b504a-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b504a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b504a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b504a-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b504a-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b504a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b504a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b504a-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b504a-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b504a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="b504a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b504a-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b504a-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b504a-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b504a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b504a-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b504a-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b504a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b504a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b504a-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b504a-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




