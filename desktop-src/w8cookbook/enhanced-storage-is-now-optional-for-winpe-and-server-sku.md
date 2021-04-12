---
title: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
description: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316596"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="3d4ae-103">Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur</span><span class="sxs-lookup"><span data-stu-id="3d4ae-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="3d4ae-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="3d4ae-104">Platforms</span></span>

<span data-ttu-id="3d4ae-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="3d4ae-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="3d4ae-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d4ae-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="3d4ae-107">Description</span><span class="sxs-lookup"><span data-stu-id="3d4ae-107">Description</span></span>

<span data-ttu-id="3d4ae-108">Le stockage étendu était toujours disponible sur les périphériques USB Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="3d4ae-109">Avec la sortie de Windows 8, il est disponible pour tous les périphériques de stockage.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="3d4ae-110">Dans les périphériques basés sur le client, il est activé par défaut. dans périphériques serveur, cette option est facultative et doit être approvisionnée via environnement de préinstallation Windows (WinPE) (WinPE).</span><span class="sxs-lookup"><span data-stu-id="3d4ae-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="3d4ae-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="3d4ae-111">Manifestation</span></span>

<span data-ttu-id="3d4ae-112">Le périphérique serveur échoue si le stockage étendu n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="3d4ae-113">Les périphériques de démarrage doivent être approvisionnés via WinPE avec cette option activée.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="3d4ae-114">Solution</span><span class="sxs-lookup"><span data-stu-id="3d4ae-114">Solution</span></span>

<span data-ttu-id="3d4ae-115">Étant donné que le stockage étendu est facultatif pour le serveur d’exécution, les développeurs doivent l’ajouter à WinPE pour l’approvisionnement et l’activation de ces lecteurs.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="3d4ae-116">Pour plus d’informations, consultez le Guide de déploiement.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-116">See the deployment guide for details.</span></span>

<span data-ttu-id="3d4ae-117">Les administrateurs de serveur doivent ensuite configurer explicitement leur serveur pour qu’ils utilisent le stockage étendu.</span><span class="sxs-lookup"><span data-stu-id="3d4ae-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




