---
title: Fonctionnement de la couche de débogage D3D12
description: Décrit comment tirer le meilleur parti de la couche de débogage D3D12.
ms.assetid: C95FABCB-BBB6-48B1-8D13-25A49A1A0C73
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 8ee5ff8ad63fc4d050d01d4d2193a7bd8dbec6ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104049"
---
# <a name="debugging-and-diagnostics-with-direct3d-12"></a><span data-ttu-id="fba9a-103">Débogage et diagnostics avec Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fba9a-103">Debugging and diagnostics with Direct3D 12</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fba9a-104">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="fba9a-104">In this section</span></span>

| <span data-ttu-id="fba9a-105">Rubrique</span><span class="sxs-lookup"><span data-stu-id="fba9a-105">Topic</span></span> | <span data-ttu-id="fba9a-106">Description</span><span class="sxs-lookup"><span data-stu-id="fba9a-106">Description</span></span> |
|-|-|
| [<span data-ttu-id="fba9a-107">Utiliser la validation basée sur GPU avec la couche de débogage Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fba9a-107">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](using-d3d12-debug-layer-gpu-based-validation.md) | <span data-ttu-id="fba9a-108">Cette rubrique explique comment tirer le meilleur parti de la couche de débogage Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="fba9a-108">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="fba9a-109">La validation basée sur GPU (GBV) active des scénarios de validation sur la chronologie GPU qui ne sont pas possibles lors des appels d’API sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="fba9a-109">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> |
| [<span data-ttu-id="fba9a-110">Utiliser ordinateur pour diagnostiquer les erreurs GPU</span><span class="sxs-lookup"><span data-stu-id="fba9a-110">Use DRED to diagnose GPU faults</span></span>](use-dred.md) | <span data-ttu-id="fba9a-111">Le ordinateur (Device removed Extended Data) est un ensemble évolutif de fonctionnalités de diagnostic conçues pour vous aider à identifier la cause des erreurs de suppression de périphérique inattendues.</span><span class="sxs-lookup"><span data-stu-id="fba9a-111">Device Removed Extended Data (DRED) is an evolving set of diagnostic features designed to help you to identify the cause of unexpected device removal errors.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="fba9a-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fba9a-112">Related topics</span></span>

* [<span data-ttu-id="fba9a-113">Référence de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="fba9a-113">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
* [<span data-ttu-id="fba9a-114">Guide de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fba9a-114">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
