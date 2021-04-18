---
title: Indicateur de test
description: Indicateur de test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Indicateur de MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311425"
---
# <a name="the-test-flag"></a><span data-ttu-id="de0ad-104">Indicateur de test</span><span class="sxs-lookup"><span data-stu-id="de0ad-104">The Test Flag</span></span>

<span data-ttu-id="de0ad-105">L’indicateur « test » ( \_ test MCI) interroge l’appareil pour déterminer s’il peut exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="de0ad-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="de0ad-106">L’appareil retourne une erreur s’il ne peut pas exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="de0ad-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="de0ad-107">Elle ne retourne aucune erreur si elle peut gérer la commande.</span><span class="sxs-lookup"><span data-stu-id="de0ad-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="de0ad-108">Lorsque vous spécifiez cet indicateur, MCI retourne le contrôle à l’application sans exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="de0ad-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="de0ad-109">Cet indicateur est pris en charge par les appareils vidéo numériques et VCR pour toutes les commandes, à l’exception de l' [**ouverture**](open.md) ([**MCI \_ Open**](mci-open.md)) et de la [**fermeture**](close.md) ([**MCI \_ Close**](mci-close.md)).</span><span class="sxs-lookup"><span data-stu-id="de0ad-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




