---
title: DOSwarmStats, structure (Deliveryoptimization. h)
description: Contient des champs pour les statistiques de téléchargement et de téléchargement d’un fichier.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- DOSwarmStats, structure
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509948"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="53c1d-104">DOSwarmStats, structure</span><span class="sxs-lookup"><span data-stu-id="53c1d-104">DOSwarmStats structure</span></span>

<span data-ttu-id="53c1d-105">Contient des champs pour les statistiques de téléchargement et de téléchargement d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="53c1d-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c1d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53c1d-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="53c1d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="53c1d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="53c1d-108">**Combinaison**</span><span class="sxs-lookup"><span data-stu-id="53c1d-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-109">Chaîne terminée par le caractère null qui a été spécifiée avec l’appel **AddFileWithRanges** .</span><span class="sxs-lookup"><span data-stu-id="53c1d-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-110">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="53c1d-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-111">Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur (par exemple, https:// &lt; Server &gt; / &lt; path &gt; /file.ext).</span><span class="sxs-lookup"><span data-stu-id="53c1d-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-112">**Taille**</span><span class="sxs-lookup"><span data-stu-id="53c1d-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-113">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="53c1d-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-114">**totalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="53c1d-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-115">Nombre total d’octets transférés.</span><span class="sxs-lookup"><span data-stu-id="53c1d-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-116">**bytesFromLanPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-117">Nombre d’octets transférés à partir d’homologues LAN.</span><span class="sxs-lookup"><span data-stu-id="53c1d-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-118">**bytesFromGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-119">Nombre d’octets transférés à partir des pairs du groupe.</span><span class="sxs-lookup"><span data-stu-id="53c1d-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-120">**bytesFromInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-121">Nombre d’octets transférés à partir d’homologues Internet.</span><span class="sxs-lookup"><span data-stu-id="53c1d-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-122">**bytesFromHttp**</span><span class="sxs-lookup"><span data-stu-id="53c1d-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-123">Nombre d’octets transférés à partir de http.</span><span class="sxs-lookup"><span data-stu-id="53c1d-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-124">**bytesFromDoinc**</span><span class="sxs-lookup"><span data-stu-id="53c1d-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-125">À usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="53c1d-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-126">**bytesToLanPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-127">Nombre d’octets transférés aux homologues LAN.</span><span class="sxs-lookup"><span data-stu-id="53c1d-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-128">**bytesToGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-129">Nombre d’octets transférés aux pairs du groupe.</span><span class="sxs-lookup"><span data-stu-id="53c1d-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-130">**bytesToInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="53c1d-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-131">Nombre d’octets transférés aux pairs Internet.</span><span class="sxs-lookup"><span data-stu-id="53c1d-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-132">**httpConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="53c1d-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-133">Nombre de connexions http.</span><span class="sxs-lookup"><span data-stu-id="53c1d-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-134">**doincConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="53c1d-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-135">À usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="53c1d-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-136">**lanConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="53c1d-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-137">Nombre de connexions LAN.</span><span class="sxs-lookup"><span data-stu-id="53c1d-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-138">**groupConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="53c1d-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-139">Nombre de connexions de groupe.</span><span class="sxs-lookup"><span data-stu-id="53c1d-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-140">**internetConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="53c1d-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-141">Nombre de connexions Internet.</span><span class="sxs-lookup"><span data-stu-id="53c1d-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-142">**downloadDuration**</span><span class="sxs-lookup"><span data-stu-id="53c1d-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-143">Durée du transfert de fichiers en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="53c1d-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-144">**downloadMode**</span><span class="sxs-lookup"><span data-stu-id="53c1d-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-145">Le mode de téléchargement utilisé, consultez [**DownloadMode**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="53c1d-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-146">**statut**</span><span class="sxs-lookup"><span data-stu-id="53c1d-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-147">L’état d’un transfert de fichiers, consultez [**SwarmStatus**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="53c1d-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="53c1d-148">**isBackground**</span><span class="sxs-lookup"><span data-stu-id="53c1d-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="53c1d-149">True, s’il s’agit d’un transfert en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="53c1d-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53c1d-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53c1d-150">Requirements</span></span>



| <span data-ttu-id="53c1d-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53c1d-151">Requirement</span></span> | <span data-ttu-id="53c1d-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c1d-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c1d-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c1d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="53c1d-154">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c1d-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53c1d-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c1d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="53c1d-156">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c1d-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="53c1d-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="53c1d-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c1d-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c1d-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





