---
title: Considérations sur la sécurité - Système de couleurs Windows
description: Considérations sur la sécurité - Système de couleurs Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Système de couleurs Windows (WCS), sécurité
- WCS (système de couleurs Windows), sécurité
- gestion des couleurs des images, sécurité
- gestion des couleurs, sécurité
- sécurité du système de couleurs Windows (WCS)
- Module de gestion des couleurs (CMM)
- CMM (module de gestion des couleurs)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106537179"
---
# <a name="security-considerations-windows-color-system"></a><span data-ttu-id="d64dc-110">Considérations relatives à la sécurité : système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="d64dc-110">Security Considerations: Windows Color System</span></span>

<span data-ttu-id="d64dc-111">Ce document fournit des informations sur les considérations de sécurité liées à la gestion des couleurs des images.</span><span class="sxs-lookup"><span data-stu-id="d64dc-111">This document provides information about security considerations related to image color management.</span></span> <span data-ttu-id="d64dc-112">Ce document ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-le plutôt comme point de départ et référence pour ce domaine technologique.</span><span class="sxs-lookup"><span data-stu-id="d64dc-112">This document doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

## <a name="non-microsoft-cmms-can-run-in-system-context"></a><span data-ttu-id="d64dc-113">Les CMMs non-Microsoft peuvent s’exécuter dans le contexte du système</span><span class="sxs-lookup"><span data-stu-id="d64dc-113">Non-Microsoft CMMs can run in system context</span></span>

<span data-ttu-id="d64dc-114">Les modules de gestion des couleurs non-Microsoft (CMMs) doivent être traités comme des pilotes d’imprimante non-Microsoft, car ils peuvent s’exécuter dans un contexte système pour les opérations d’impression.</span><span class="sxs-lookup"><span data-stu-id="d64dc-114">Non-Microsoft Color Management Modules (CMMs) should be treated like non-Microsoft printer drivers because they have the potential to run in a system context for printing operations.</span></span>
