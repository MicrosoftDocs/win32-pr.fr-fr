---
description: Une palette de couleurs est un tableau qui contient des valeurs de couleur identifiant les couleurs qui peuvent actuellement être affichées ou dessinées sur le périphérique de sortie.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Palettes de couleurs (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114695"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="6b540-103">Palettes de couleurs (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="6b540-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="6b540-104">Une palette de couleurs est un tableau qui contient des valeurs de couleur identifiant les couleurs qui peuvent actuellement être affichées ou dessinées sur le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="6b540-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="6b540-105">Les palettes de couleurs sont utilisées par les appareils capables de générer de nombreuses couleurs, mais qui ne peuvent afficher ou dessiner qu’un sous-ensemble de ces couleurs à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="6b540-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="6b540-106">Pour ces appareils, le système gère une *palette système* pour suivre et gérer les couleurs actuelles de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6b540-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="6b540-107">Les applications n’ont pas d’accès direct à la palette du système.</span><span class="sxs-lookup"><span data-stu-id="6b540-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="6b540-108">Au lieu de cela, le système associe une palette par défaut à chaque contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6b540-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="6b540-109">Les applications peuvent utiliser les couleurs de la palette par défaut ou définir leurs propres couleurs en créant des *palettes logiques* et en les associant à des contextes de périphérique individuels.</span><span class="sxs-lookup"><span data-stu-id="6b540-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="6b540-110">Une application peut déterminer si un appareil prend en charge les palettes de couleurs en recherchant le \_ bit de palette RC dans la valeur RasterCaps retournée par la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="6b540-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



