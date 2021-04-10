---
description: L’objet Merge permet d’accéder à d’autres objets de niveau supérieur. Un objet de fusion doit être créé avant le chargement de la prise en charge d’Automation requise par COM pour accéder aux fonctions dans Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Objet Merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210591"
---
# <a name="merge-object"></a><span data-ttu-id="def11-104">Objet Merge</span><span class="sxs-lookup"><span data-stu-id="def11-104">Merge Object</span></span>

<span data-ttu-id="def11-105">L’objet **Merge** permet d’accéder à d’autres objets de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="def11-105">The **Merge** object provides access to other top-level objects.</span></span> <span data-ttu-id="def11-106">Un objet de **fusion** doit être créé avant le chargement de la prise en charge d’Automation requise par com pour accéder aux fonctions dans Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="def11-106">A **Merge** object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.</span></span>

<span data-ttu-id="def11-107">Mergemod.dll permet d’accéder aux fonctionnalités étendues au moment de la génération par le biais d’une deuxième version du CLSID existant.</span><span class="sxs-lookup"><span data-stu-id="def11-107">Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID.</span></span> <span data-ttu-id="def11-108">Ce CLSID prend en charge les fonctionnalités existantes disponibles via l’interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , mais l’interface par défaut sur l’objet (et l’interface double associée) est l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) au lieu de l’interface **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="def11-108">This CLSID supports existing functionality available through the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) interface, but the default interface on the object (and the associated dual interface) is the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface instead of the **IMsmMerge** interface.</span></span>

 

 
