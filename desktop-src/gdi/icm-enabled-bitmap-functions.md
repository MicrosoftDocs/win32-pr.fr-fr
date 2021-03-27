---
description: La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled les fonctions bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863638"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="a069e-103">ICM-Enabled les fonctions bitmap</span><span class="sxs-lookup"><span data-stu-id="a069e-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="a069e-104">La gestion des couleurs ICM (Microsoft Image Color Management) garantit qu’une image de couleur, un objet graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="a069e-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="a069e-105">Que vous scanniez une image ou un autre graphique sur un scanneur de couleurs, que vous la téléchargeiez sur Internet, que vous la visualisiez ou la modifiiez à l’écran, ou que vous l’imprimiez sur papier, film ou autre média, ICM 2,0 vous aide à maintenir la cohérence et la précision des couleurs.</span><span class="sxs-lookup"><span data-stu-id="a069e-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="a069e-106">Pour plus d’informations sur ICM, consultez [système de couleurs Windows](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a069e-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="a069e-107">Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur.</span><span class="sxs-lookup"><span data-stu-id="a069e-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="a069e-108">Les fonctions bitmap suivantes sont activées pour une utilisation avec ICM :</span><span class="sxs-lookup"><span data-stu-id="a069e-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="a069e-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="a069e-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="a069e-110">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="a069e-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="a069e-111">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="a069e-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="a069e-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="a069e-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="a069e-113">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="a069e-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="a069e-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="a069e-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="a069e-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="a069e-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="a069e-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="a069e-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="a069e-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="a069e-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
