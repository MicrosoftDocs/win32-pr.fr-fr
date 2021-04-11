---
title: Énumération DownloadMode (Deliveryoptimization. h)
description: Définit les différents modes de téléchargement utilisés par l’optimisation de la distribution.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Permet de contourner l’optimisation de la distribution et d’utiliser la fonction BITS, à la place. Par exemple, sélectionnez ce mode pour que les clients puissent utiliser BranchCache. énumération
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032778"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="39b89-106">Énumération DownloadMode</span><span class="sxs-lookup"><span data-stu-id="39b89-106">DownloadMode enumeration</span></span>

<span data-ttu-id="39b89-107">Définit les différents modes de téléchargement utilisés par l’optimisation de la distribution.</span><span class="sxs-lookup"><span data-stu-id="39b89-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39b89-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="39b89-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="39b89-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="39b89-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="39b89-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-111">Ce paramètre désactive la mise en cache d’égal à égal, mais permet toujours l’optimisation de la distribution pour télécharger le contenu à partir des serveurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39b89-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="39b89-112">Ce mode utilise des métadonnées supplémentaires fournies par les services Cloud d’optimisation de la livraison pour une expérience de téléchargement fiable et efficace Peerless.</span><span class="sxs-lookup"><span data-stu-id="39b89-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="39b89-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-114">Ce mode de fonctionnement par défaut permet le partage entre des pairs d’un même réseau.</span><span class="sxs-lookup"><span data-stu-id="39b89-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="39b89-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-116">Lorsque le mode groupe est défini, le groupe est automatiquement sélectionné en fonction du site s Active Directory Domain Services (AD DS) du périphérique (Windows 10, version 1607) ou du domaine auquel l’appareil est authentifié (Windows 10, version 1511).</span><span class="sxs-lookup"><span data-stu-id="39b89-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="39b89-117">En mode Groupe, le peering est effectué sur des sous-réseaux internes, entre les appareils qui appartiennent au même groupe. Cela inclut les appareils situés dans des bureaux distants.</span><span class="sxs-lookup"><span data-stu-id="39b89-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="39b89-118">Vous pouvez utiliser l’option GroupID pour créer votre propre groupe personnalisé, indépendamment des domaines et des sites AD DS.</span><span class="sxs-lookup"><span data-stu-id="39b89-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="39b89-119">Le mode de téléchargement groupé est l’option recommandée pour la plupart des organisations qui recherchent la meilleure optimisation de la bande passante avec l’Optimisation de la distribution.</span><span class="sxs-lookup"><span data-stu-id="39b89-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="39b89-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-121">Active les sources homologues Internet pour l’optimisation de la distribution.</span><span class="sxs-lookup"><span data-stu-id="39b89-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="39b89-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-123">Le mode Simple désactive entièrement les services cloud de la fonction d’optimisation de la distribution (dans le cas des environnements hors ligne).</span><span class="sxs-lookup"><span data-stu-id="39b89-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="39b89-124">L’optimisation de la distribution bascule automatiquement vers ce mode lorsque les services Cloud d’optimisation de la distribution ne sont pas disponibles, sont inaccessibles ou lorsque la taille du fichier de contenu est inférieure à 10 Mo.</span><span class="sxs-lookup"><span data-stu-id="39b89-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="39b89-125">Dans ce mode, l’optimisation de la distribution fournit une expérience de téléchargement fiable, sans mise en cache d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="39b89-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="39b89-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="39b89-127">Permet de contourner l’optimisation de la distribution et d’utiliser la fonction BITS, à la place.</span><span class="sxs-lookup"><span data-stu-id="39b89-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="39b89-128">Par exemple, sélectionnez ce mode pour que les clients puissent utiliser BranchCache.</span><span class="sxs-lookup"><span data-stu-id="39b89-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39b89-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39b89-129">Requirements</span></span>

| <span data-ttu-id="39b89-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39b89-130">Requirement</span></span> | <span data-ttu-id="39b89-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b89-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="39b89-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b89-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39b89-133">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b89-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="39b89-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b89-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39b89-135">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b89-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="39b89-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="39b89-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b89-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
