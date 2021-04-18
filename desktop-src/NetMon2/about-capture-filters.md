---
description: Un filtre de capture est un élément d’une application NPP qui indique au pilote de Moniteur réseau (Nmnt.sys) les trames de données réseau à conserver et les trames à ignorer.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: À propos des filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536365"
---
# <a name="about-capture-filters"></a><span data-ttu-id="1d20b-103">À propos des filtres de capture</span><span class="sxs-lookup"><span data-stu-id="1d20b-103">About Capture Filters</span></span>

<span data-ttu-id="1d20b-104">Un filtre de capture est un élément d’une application NPP qui indique au pilote de Moniteur réseau (Nmnt.sys) les trames de données réseau à conserver et les trames à ignorer.</span><span class="sxs-lookup"><span data-stu-id="1d20b-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="1d20b-105">L’avantage de définir un filtre de capture est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="1d20b-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="1d20b-106">Vous n’avez pas besoin d’examiner les frames capturés. le pilote Moniteur réseau les examine.</span><span class="sxs-lookup"><span data-stu-id="1d20b-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="1d20b-107">Cette approche élimine la copie de frame, qui offre un avantage de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1d20b-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="1d20b-108">Structure de filtre de capture</span><span class="sxs-lookup"><span data-stu-id="1d20b-108">Capture Filter Structure</span></span>

<span data-ttu-id="1d20b-109">Les filtres de capture se composent de trois éléments :</span><span class="sxs-lookup"><span data-stu-id="1d20b-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="1d20b-110">Paramètres ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="1d20b-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="1d20b-111">Adresse</span><span class="sxs-lookup"><span data-stu-id="1d20b-111">Address</span></span>
-   <span data-ttu-id="1d20b-112">Correspondance de modèle</span><span class="sxs-lookup"><span data-stu-id="1d20b-112">Pattern match</span></span>

<span data-ttu-id="1d20b-113">Ensemble, ces éléments évaluent logiquement les frames à inclure ou à exclure au cours de l’opération d’une application NPP.</span><span class="sxs-lookup"><span data-stu-id="1d20b-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="1d20b-114">Le filtre de capture fournit des correspondances et des exclusions complexes d’éléments de frame à l’application NPP.</span><span class="sxs-lookup"><span data-stu-id="1d20b-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="1d20b-115">Moniteur réseau implémente le filtre de capture via une structure de données, [**capturefilter**](the-capturefilter-structure.md), passée au NPP, puis transmis au pilote Moniteur réseau au démarrage de la capture.</span><span class="sxs-lookup"><span data-stu-id="1d20b-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="1d20b-116">Pour plus d’informations sur les opérations NPP et les fonctionnalités d’objet BLOB, consultez [fournisseurs de paquets réseau](network-packet-providers.md) et [objets BLOB de moniteur réseau](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="1d20b-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



