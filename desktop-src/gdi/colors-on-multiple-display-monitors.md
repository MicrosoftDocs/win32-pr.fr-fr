---
description: Chaque analyse peut avoir sa propre profondeur de couleur.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Couleurs sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951560"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="63ac9-103">Couleurs sur plusieurs moniteurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="63ac9-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="63ac9-104">Chaque analyse peut avoir sa propre profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="63ac9-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="63ac9-105">Le système ajuste automatiquement les couleurs au fur et à mesure que les fenêtres passent par les moniteurs avec des profondeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="63ac9-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="63ac9-106">En général, cela produit de bons résultats.</span><span class="sxs-lookup"><span data-stu-id="63ac9-106">In general, this produces good results.</span></span> <span data-ttu-id="63ac9-107">Toutefois, cela n’est pas toujours optimal.</span><span class="sxs-lookup"><span data-stu-id="63ac9-107">However, this is not always optimal.</span></span> <span data-ttu-id="63ac9-108">Pour tirer parti des fonctionnalités de couleur des différents moniteurs, consultez la section [peinture sur plusieurs écrans d’affichage](painting-on-multiple-display-monitors.md) qui suit.</span><span class="sxs-lookup"><span data-stu-id="63ac9-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="63ac9-109">Pour déterminer si toutes les analyses ont le même format de couleur, appelez [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le SM \_ SAMEDISPLAYFORMAT.</span><span class="sxs-lookup"><span data-stu-id="63ac9-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="63ac9-110">Si l’analyse principale est en palette, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) fonctionnent de la même manière qu’auparavant, mais sur toutes les analyses.</span><span class="sxs-lookup"><span data-stu-id="63ac9-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="63ac9-111">En outre, les palettes de tous les appareils en palette sont synchronisées.</span><span class="sxs-lookup"><span data-stu-id="63ac9-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="63ac9-112">Si le moniteur principal n’est pas en palette, **SelectPalette** et **RealizePalette** sélectionnent la palette dans l’arrière-plan et les appareils en palette ne sont pas synchronisés.</span><span class="sxs-lookup"><span data-stu-id="63ac9-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
