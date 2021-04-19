---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Bibliothèque de Registre hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517181"
---
# <a name="offline-registry-library"></a><span data-ttu-id="c7f71-103">Bibliothèque de Registre hors connexion</span><span class="sxs-lookup"><span data-stu-id="c7f71-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="c7f71-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="c7f71-104">Purpose</span></span>

<span data-ttu-id="c7f71-105">La bibliothèque de Registre hors connexion (Offreg.dll) est utilisée pour modifier une ruche de registre en dehors du Registre système actif.</span><span class="sxs-lookup"><span data-stu-id="c7f71-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="c7f71-106">Cette bibliothèque est destinée aux scénarios de mise à jour du Registre tels que la maintenance d’une image du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c7f71-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="c7f71-107">La bibliothèque prend en charge les formats Hive de Registre à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7f71-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c7f71-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="c7f71-108">Developer audience</span></span>

<span data-ttu-id="c7f71-109">Cette technologie est destinée aux fabricants OEM (Original Equipment Manufacturers), aux éditeurs de logiciels anti-programme malveillant et à d’autres développeurs d’applications qui doivent être en mesure d’analyser les fichiers ruche du registre sans les charger dans le Registre actif.</span><span class="sxs-lookup"><span data-stu-id="c7f71-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c7f71-110">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="c7f71-110">Run-time requirements</span></span>

<span data-ttu-id="c7f71-111">La bibliothèque de Registre hors connexion est fournie sous la forme d’une bibliothèque de liens dynamiques (DLL) redistribuable binaire.</span><span class="sxs-lookup"><span data-stu-id="c7f71-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="c7f71-112">Cette bibliothèque s’exécute sur les versions suivantes de Windows :</span><span class="sxs-lookup"><span data-stu-id="c7f71-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="c7f71-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c7f71-113">Windows Server 2016</span></span>  
<span data-ttu-id="c7f71-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c7f71-114">Windows 10</span></span>  
<span data-ttu-id="c7f71-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c7f71-115">Windows 8.1</span></span>  
<span data-ttu-id="c7f71-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c7f71-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="c7f71-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7f71-117">Windows 8</span></span>  
<span data-ttu-id="c7f71-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7f71-118">Windows Server 2012</span></span>  
<span data-ttu-id="c7f71-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c7f71-119">Windows 7</span></span>  
<span data-ttu-id="c7f71-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7f71-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="c7f71-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7f71-121">Windows Server 2008</span></span>  
<span data-ttu-id="c7f71-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7f71-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="c7f71-123">Les applications doivent être liées à Offreg.dll à l’aide de la liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="c7f71-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="c7f71-124">Offreg.dll est fourni dans le kit de pilotes Windows (WDK) pour Windows 10 et les versions antérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="c7f71-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="c7f71-125">Pour plus d’informations sur l’obtention du kit WDK, consultez [Comment obtenir le kit WDK et le WLK](/windows-hardware/drivers/download-the-wdk) ou visitez le site Web des [abonnements MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c7f71-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7f71-126">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c7f71-126">In this section</span></span>

-   [<span data-ttu-id="c7f71-127">**À propos de la bibliothèque de Registre hors connexion**</span><span class="sxs-lookup"><span data-stu-id="c7f71-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="c7f71-128">**Fonctions de la bibliothèque de Registre hors connexion**</span><span class="sxs-lookup"><span data-stu-id="c7f71-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
