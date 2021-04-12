---
title: Modification de la position actuelle
description: Modification de la position actuelle
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381966"
---
# <a name="changing-the-current-position"></a><span data-ttu-id="af133-104">Modification de la position actuelle</span><span class="sxs-lookup"><span data-stu-id="af133-104">Changing the Current Position</span></span>

<span data-ttu-id="af133-105">Pour modifier la position actuelle dans un élément d’appareil, utilisez le message de commande [**MCI \_ Seek**](mci-seek.md) avec l’MCI \_ pour marquer et la structure de [**\_ recherche MCI Seek \_**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="af133-105">To change the current position in a device element, use the [**MCI\_SEEK**](mci-seek.md) command message along with the MCI\_TO flag and the [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="af133-106">Si vous utilisez le membre **dwTo** pour spécifier une position de recherche avec MCI \_ Seek, vous devez interroger le format d’heure et le définir, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af133-106">If you use the **dwTo** member to specify a seek position with MCI\_SEEK, you should query the time format and set it, if necessary.</span></span>

<span data-ttu-id="af133-107">En plus de spécifier une position avec le membre **dwTo** , vous pouvez spécifier la \_ recherche MCI \_ pour \_ Démarrer ou MCI \_ Rechercher les \_ indicateurs de \_ fin pour le paramètre *dwParam1* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) afin de rechercher les positions de début et de fin de l’élément d’appareil.</span><span class="sxs-lookup"><span data-stu-id="af133-107">In addition to specifying a position with the **dwTo** member, you can specify the MCI\_SEEK\_TO\_START or MCI\_SEEK\_TO\_END flags for the *dwParam1* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to find the starting and ending positions of the device element.</span></span> <span data-ttu-id="af133-108">Si vous utilisez l’un de ces indicateurs, ne spécifiez pas l' \_ indicateur MCI.</span><span class="sxs-lookup"><span data-stu-id="af133-108">If you use one of these flags, don't specify the MCI\_TO flag.</span></span>

 

 