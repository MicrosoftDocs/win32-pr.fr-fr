---
description: 'IESP :: Stop, méthode : la méthode Stop arrête la capture en cours.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103767"
---
# <a name="iespstop-method"></a><span data-ttu-id="72faf-103">IESP :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="72faf-103">IESP::Stop method</span></span>

<span data-ttu-id="72faf-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="72faf-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="72faf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72faf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="72faf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72faf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72faf-107">*lpStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="72faf-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72faf-108">Pointeur vers une structure de [statistiques](statistics.md) qui contient des statistiques réseau, telles que les trames totales et le nombre total d’octets capturés.</span><span class="sxs-lookup"><span data-stu-id="72faf-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72faf-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72faf-109">Return value</span></span>

<span data-ttu-id="72faf-110">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="72faf-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="72faf-111">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="72faf-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="72faf-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="72faf-112">Return code</span></span>                                                                                          | <span data-ttu-id="72faf-113">Description</span><span class="sxs-lookup"><span data-stu-id="72faf-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72faf-114"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="72faf-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="72faf-115">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="72faf-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="72faf-116">Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="72faf-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="72faf-117"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="72faf-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="72faf-118">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="72faf-118">The NPP is not capturing data.</span></span> <span data-ttu-id="72faf-119">Appelez [IESP :: Start](iesp-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="72faf-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="72faf-120"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="72faf-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="72faf-121">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="72faf-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="72faf-122">Notes </span><span class="sxs-lookup"><span data-stu-id="72faf-122">Remarks</span></span>

<span data-ttu-id="72faf-123">Quand la méthode **IESP :: Stop** est appelée, moniteur réseau arrête la capture des données et ferme le [*fichier de capture.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="72faf-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="72faf-124">(Le nom du fichier de capture a été retourné lors de l’appel de [IESP :: Start](iesp-start.md) .) Vous pouvez maintenant examiner le contenu du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="72faf-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="72faf-125">Lorsque vous arrêtez et redémarrez la capture, veillez à appeler la méthode [IESP :: configure](iesp-configure.md) chaque fois que vous appelez [IESP :: Start](iesp-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="72faf-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="72faf-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72faf-126">Requirements</span></span>



| <span data-ttu-id="72faf-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72faf-127">Requirement</span></span> | <span data-ttu-id="72faf-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="72faf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72faf-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72faf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72faf-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72faf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="72faf-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72faf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72faf-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72faf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="72faf-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="72faf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="72faf-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="72faf-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="72faf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="72faf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72faf-136"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72faf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72faf-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72faf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72faf-138">IESP</span><span class="sxs-lookup"><span data-stu-id="72faf-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="72faf-139">IESP :: Connect</span><span class="sxs-lookup"><span data-stu-id="72faf-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="72faf-140">IESP :: Start</span><span class="sxs-lookup"><span data-stu-id="72faf-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="72faf-141">PORTENT</span><span class="sxs-lookup"><span data-stu-id="72faf-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




