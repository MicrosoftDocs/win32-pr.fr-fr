---
description: TAPI 2,0 fournit un petit nombre d’améliorations apportées à la fonctionnalité de base de l’interface TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319146"
---
# <a name="tapi-20"></a><span data-ttu-id="d7310-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="d7310-103">TAPI 2.0</span></span>

<span data-ttu-id="d7310-104">TAPI 2,0 fournit un petit nombre d’améliorations apportées à la fonctionnalité de base de l’interface TAPI 1,4.</span><span class="sxs-lookup"><span data-stu-id="d7310-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="d7310-105">Toutefois, il y avait des modifications architecturales majeures qui ont beaucoup amélioré sa stabilité.</span><span class="sxs-lookup"><span data-stu-id="d7310-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="d7310-106">La plupart des modifications étaient des modifications fondamentales nécessaires pour mettre l’interface TAPI sur Windows NT 4,0 et tirer parti de ses fonctionnalités (prise en charge complète de 32 bits, services et Unicode).</span><span class="sxs-lookup"><span data-stu-id="d7310-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="d7310-107">Toutefois, ces modifications étaient internes à l’interface TAPI et avaient peu d’effet sur les applications TAPI.</span><span class="sxs-lookup"><span data-stu-id="d7310-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="d7310-108">Les applications qui prennent en charge l’interface TAPI 1,3 et 1,4 (applications 16 bits par le biais d’une couche de conversion) fonctionnent bien sur les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000 et Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d7310-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="d7310-109">Toutefois, l’effet sur les développeurs de fournisseurs de services était important.</span><span class="sxs-lookup"><span data-stu-id="d7310-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="d7310-110">Les fournisseurs de services pour ces systèmes d’exploitation doivent être des dll Unicode entièrement 32 bits qui peuvent s’exécuter dans le contexte de TAPISRV, et non dans le contexte de l’application TAPI (comme pour tous les TSPs basés sur Win16 précédents).</span><span class="sxs-lookup"><span data-stu-id="d7310-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="d7310-111">TSPs conçu pour TAPI 1,4 ne fonctionne pas sur les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000 ou Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d7310-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="d7310-112">TAPI 2,0 ajoute également les fonctionnalités importantes de la prise en charge du centre d’appels et de la qualité de service (QOS).</span><span class="sxs-lookup"><span data-stu-id="d7310-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="d7310-113">Les binaires système TAPI fournis avec Windows prennent en charge TAPI versions 1,3 et 1,4 pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="d7310-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="d7310-114">Toutefois, les applications 16 bits ne peuvent pas utiliser TAPI 2,0 et vous ne pouvez pas utiliser un TSP TAPI 2. x de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d7310-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



