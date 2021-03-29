---
description: Parmi les six modes de mappage prédéfinis, l’un est dépendant du périphérique (texte de MM \_ ) et les cinq autres (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC et mm \_ TWIPS) sont indépendants des appareils.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modes de mappage prédéfinis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972563"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="b5e58-103">Modes de mappage prédéfinis</span><span class="sxs-lookup"><span data-stu-id="b5e58-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="b5e58-104">Parmi les six modes de mappage prédéfinis, l’un est dépendant du périphérique (texte de MM \_ ) et les cinq autres (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC et mm \_ TWIPS) sont indépendants des appareils.</span><span class="sxs-lookup"><span data-stu-id="b5e58-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="b5e58-105">Le mode de mappage par défaut est le texte de MM \_ .</span><span class="sxs-lookup"><span data-stu-id="b5e58-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="b5e58-106">Une unité logique est égale à un pixel.</span><span class="sxs-lookup"><span data-stu-id="b5e58-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="b5e58-107">Le x positif est à droite, et le y positif est inactif.</span><span class="sxs-lookup"><span data-stu-id="b5e58-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="b5e58-108">Ce mode est mappé directement au système de coordonnées de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b5e58-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="b5e58-109">Le mappage logique-physique implique uniquement un décalage en x et y qui est défini par la fenêtre contrôlée par l’application et les origines de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b5e58-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="b5e58-110">La fenêtre d’affichage et les étendues de fenêtre ont toutes la valeur 1, ce qui crée un mappage un-à-un.</span><span class="sxs-lookup"><span data-stu-id="b5e58-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="b5e58-111">Les applications qui affichent des formes géométriques (cercles, carrés, polygones, etc.) utilisent l’un des modes de mappage indépendants du périphérique.</span><span class="sxs-lookup"><span data-stu-id="b5e58-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="b5e58-112">Par exemple, si vous écrivez une application pour fournir des fonctionnalités graphiques à un programme de feuille de calcul et que vous souhaitez vous assurer que le diamètre de chaque graphique à secteurs est de 2 pouces, utilisez le \_ mode de mappage mm LOENGLISH et appelez les fonctions appropriées pour dessiner et remplir le graphique.</span><span class="sxs-lookup"><span data-stu-id="b5e58-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="b5e58-113">Si vous spécifiez MM \_ LOENGLISH, vous garantissez que le diamètre du graphique est cohérent sur l’écran ou l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b5e58-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="b5e58-114">Si le \_ texte de mm est utilisé à la place de mm \_ LOENGLISH, un graphique qui apparaît circulaire sur un écran VGA apparaîtra elliptique sur un écran EGA et serait très petit sur une imprimante laser 300 ppp (points par pouce).</span><span class="sxs-lookup"><span data-stu-id="b5e58-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



