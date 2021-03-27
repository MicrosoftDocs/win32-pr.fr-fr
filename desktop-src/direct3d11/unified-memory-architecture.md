---
title: Architecture de la mémoire unifiée
description: L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939715"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="8583a-103">Architecture de la mémoire unifiée</span><span class="sxs-lookup"><span data-stu-id="8583a-103">Unified Memory Architecture</span></span>

<span data-ttu-id="8583a-104">L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.</span><span class="sxs-lookup"><span data-stu-id="8583a-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="8583a-105">Une valeur booléenne, définie par le pilote, peut être lue à partir de la structure de données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) pour déterminer si le matériel prend en charge la UMA.</span><span class="sxs-lookup"><span data-stu-id="8583a-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="8583a-106">Les applications qui s’exécutent sur une UMA peuvent souhaiter avoir plus de ressources avec un accès processeur activé que si elles ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="8583a-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="8583a-107">La UMA permet aux applications de ne pas copier les données des ressources, au lieu de rester efficaces uniquement pour les cartes graphiques non UMA.</span><span class="sxs-lookup"><span data-stu-id="8583a-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="8583a-108">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="8583a-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="8583a-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8583a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8583a-110">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="8583a-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




