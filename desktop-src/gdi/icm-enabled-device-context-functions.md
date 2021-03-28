---
description: La gestion des couleurs ICM (Image Color Management) de Microsoft garantit qu’une image de couleur, un graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les fonctionnalités de couleur entre les appareils.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled les fonctions de contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972663"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="340db-103">ICM-Enabled les fonctions de contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="340db-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="340db-104">La gestion des couleurs ICM (Image Color Management) de Microsoft garantit qu’une image de couleur, un graphique ou un objet texte est rendu aussi fidèlement que possible à son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les fonctionnalités de couleur entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="340db-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="340db-105">(Pour plus d’informations, consultez [système de couleurs Windows](/previous-versions//dd372446(v=vs.85)).)</span><span class="sxs-lookup"><span data-stu-id="340db-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="340db-106">Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur.</span><span class="sxs-lookup"><span data-stu-id="340db-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="340db-107">Les fonctions de contexte de périphérique suivantes sont activées pour une utilisation avec ICM :</span><span class="sxs-lookup"><span data-stu-id="340db-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="340db-108">**CreateCompatibleDC**</span><span class="sxs-lookup"><span data-stu-id="340db-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="340db-109">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="340db-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="340db-110">**GetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="340db-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="340db-111">**GetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="340db-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="340db-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="340db-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="340db-113">**SélectionnerObjet**</span><span class="sxs-lookup"><span data-stu-id="340db-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="340db-114">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="340db-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="340db-115">**SetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="340db-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
