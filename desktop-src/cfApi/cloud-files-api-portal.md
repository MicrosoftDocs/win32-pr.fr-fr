---
description: L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Moteurs de synchronisation Cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549594"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="e06a6-103">Moteurs de synchronisation Cloud</span><span class="sxs-lookup"><span data-stu-id="e06a6-103">Cloud Sync Engines</span></span>

<span data-ttu-id="e06a6-104">Voir également [exemple Cloud Mirror](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="e06a6-104">Also see [Cloud Mirror sample](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span></span>

<span data-ttu-id="e06a6-105">À compter de Windows 10, version 1709, Windows fournit l' *API de fichiers Cloud*.</span><span class="sxs-lookup"><span data-stu-id="e06a6-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="e06a6-106">Cette API est constituée de plusieurs API Win32 et WinRT natives qui formalisent la prise en charge des moteurs de synchronisation Cloud et gèrent des tâches telles que la création et la gestion de fichiers et de répertoires d’espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="e06a6-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="e06a6-107">Les utilisateurs de cette API sont généralement des fournisseurs de synchronisation et, dans une certaine mesure, des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="e06a6-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e06a6-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e06a6-108">In this section</span></span>

| <span data-ttu-id="e06a6-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e06a6-109">Topic</span></span>                                                                | <span data-ttu-id="e06a6-110">Description</span><span class="sxs-lookup"><span data-stu-id="e06a6-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e06a6-111">Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé</span><span class="sxs-lookup"><span data-stu-id="e06a6-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="e06a6-112">Découvrez comment utiliser l’API de fichiers Cloud pour créer un moteur de synchronisation de fichiers Cloud qui comprend des fichiers d’espace réservé et l’intégration de l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e06a6-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="e06a6-113">Référence du filtre Cloud</span><span class="sxs-lookup"><span data-stu-id="e06a6-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="e06a6-114">L’API de filtre Cloud est une API Win32 native qui fait partie de l’API de fichiers Cloud plus étendue.</span><span class="sxs-lookup"><span data-stu-id="e06a6-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="e06a6-115">L’API de filtre Cloud fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e06a6-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="e06a6-116">Cette API gère la création et la gestion de fichiers et de répertoires d’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="e06a6-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |