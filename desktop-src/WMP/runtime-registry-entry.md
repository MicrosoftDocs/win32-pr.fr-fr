---
title: Entrée du Registre du Runtime
description: Entrée du Registre du Runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Lecteur Windows Media, entrées de Registre du Runtime
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées du Runtime
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- entrées de Registre du Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029455"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="f9447-111">Entrée du Registre du Runtime</span><span class="sxs-lookup"><span data-stu-id="f9447-111">Runtime Registry Entry</span></span>

<span data-ttu-id="f9447-112">Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="f9447-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="f9447-113">La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f9447-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="f9447-114">L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **Runtime** .</span><span class="sxs-lookup"><span data-stu-id="f9447-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="f9447-115">L’entrée **Runtime** spécifie la technologie sous-jacente que le lecteur Windows Media peut utiliser pour lire ou convertir des fichiers multimédias numériques qui ont l’extension personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f9447-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="f9447-116">L’entrée d' **exécution** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="f9447-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="f9447-117">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f9447-117">**Name**</span></span> | <span data-ttu-id="f9447-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f9447-118">**Type**</span></span>       | <span data-ttu-id="f9447-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f9447-119">**Value**</span></span>                                                     |
| <span data-ttu-id="f9447-120">Runtime</span><span class="sxs-lookup"><span data-stu-id="f9447-120">Runtime</span></span>  | <span data-ttu-id="f9447-121">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f9447-121">**REG\_DWORD**</span></span> | <span data-ttu-id="f9447-122">Entier positif qui identifie la technologie sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="f9447-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="f9447-123">La valeur de l’entrée d' **exécution** doit être l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9447-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="f9447-124">**Valeur (décimal)**</span><span class="sxs-lookup"><span data-stu-id="f9447-124">**Value (decimal)**</span></span> | <span data-ttu-id="f9447-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9447-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9447-126">6</span><span class="sxs-lookup"><span data-stu-id="f9447-126">6</span></span>                   | <span data-ttu-id="f9447-127">Rendu à l’aide du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="f9447-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="f9447-128">7</span><span class="sxs-lookup"><span data-stu-id="f9447-128">7</span></span>                   | <span data-ttu-id="f9447-129">Rendu à l’aide de Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f9447-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="f9447-130">13</span><span class="sxs-lookup"><span data-stu-id="f9447-130">13</span></span>                  | <span data-ttu-id="f9447-131">Convertit le fichier à l’aide du plug-in de conversion spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9447-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="f9447-132">Requiert le lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="f9447-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="f9447-133">Les valeurs 6 et 7 de l’entrée de Registre du **Runtime** sont prises en charge par le lecteur Windows Media série 9 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f9447-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="f9447-134">La valeur 13 est prise en charge par le lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="f9447-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9447-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9447-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9447-136">**Sous-clé ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="f9447-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="f9447-137">**Paramètres de registre de l’extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="f9447-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




