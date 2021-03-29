---
description: Les fonctionnalités de couleur des appareils, telles que les affichages et les imprimantes, peuvent aller de monochrome à des milliers de couleurs.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Notions de base des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202049"
---
# <a name="color-basics"></a><span data-ttu-id="236ba-103">Notions de base des couleurs</span><span class="sxs-lookup"><span data-stu-id="236ba-103">Color Basics</span></span>

<span data-ttu-id="236ba-104">Les fonctionnalités de couleur des appareils, telles que les affichages et les imprimantes, peuvent aller de monochrome à des milliers de couleurs.</span><span class="sxs-lookup"><span data-stu-id="236ba-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="236ba-105">Étant donné qu’une application peut avoir besoin de générer une sortie pour des appareils dans cette plage, elle doit être préparée à gérer des fonctionnalités de couleur variables.</span><span class="sxs-lookup"><span data-stu-id="236ba-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="236ba-106">Une application peut découvrir le nombre de couleurs disponibles pour un appareil donné à l’aide de la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pour récupérer la valeur NUMCOLORS.</span><span class="sxs-lookup"><span data-stu-id="236ba-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="236ba-107">Cette valeur spécifie le nombre de couleurs pouvant être utilisées par l’application.</span><span class="sxs-lookup"><span data-stu-id="236ba-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="236ba-108">En règle générale, ce nombre correspond à une propriété physique du périphérique de sortie, par exemple le nombre d’encres de l’imprimante ou le nombre de signaux de couleur distincts que la carte vidéo peut transmettre à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="236ba-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="236ba-109">Bien que la valeur NUMCOLORS spécifie le nombre de couleurs, elle n’identifie pas les couleurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="236ba-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="236ba-110">Une application peut découvrir les couleurs disponibles en énumérant tous les stylets ayant le \_ type solide PS.</span><span class="sxs-lookup"><span data-stu-id="236ba-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="236ba-111">Étant donné que le pilote de périphérique qui prend en charge un appareil donné possède généralement une gamme complète de stylets pleins et que le système nécessite que les plumes solides aient uniquement des couleurs que l’appareil peut générer, l’énumération de ces stylets est souvent équivalente à l’énumération des couleurs.</span><span class="sxs-lookup"><span data-stu-id="236ba-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="236ba-112">Une application peut énumérer les stylets à l’aide de la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .</span><span class="sxs-lookup"><span data-stu-id="236ba-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="236ba-113">Pour obtenir un exemple de code, consultez [énumération des couleurs](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="236ba-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="236ba-114">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="236ba-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="236ba-115">Valeurs de couleur</span><span class="sxs-lookup"><span data-stu-id="236ba-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="236ba-116">Approximations de couleurs et tramage</span><span class="sxs-lookup"><span data-stu-id="236ba-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="236ba-117">Couleur dans les bitmaps</span><span class="sxs-lookup"><span data-stu-id="236ba-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="236ba-118">Mélange de couleurs</span><span class="sxs-lookup"><span data-stu-id="236ba-118">Color Mixing</span></span>](color-mixing.md)

 

 



