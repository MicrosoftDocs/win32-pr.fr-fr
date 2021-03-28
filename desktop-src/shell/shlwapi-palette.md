---
description: Cette section décrit les fonctions de gestion de la palette de couleurs du shell Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion de palette de couleurs de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203254"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="d3cd5-104">Fonctions de gestion de palette de couleurs de Shell</span><span class="sxs-lookup"><span data-stu-id="d3cd5-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="d3cd5-105">Cette section décrit les fonctions de gestion de la palette de couleurs du shell Windows.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="d3cd5-106">Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3cd5-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d3cd5-107">In this section</span></span>



| <span data-ttu-id="d3cd5-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d3cd5-108">Topic</span></span>                                                           | <span data-ttu-id="d3cd5-109">Description</span><span class="sxs-lookup"><span data-stu-id="d3cd5-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3cd5-110">**ColorAdjustLuma**</span><span class="sxs-lookup"><span data-stu-id="d3cd5-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="d3cd5-111">Modifie la luminance d’une valeur RVB.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="d3cd5-112">La teinte et la saturation ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="d3cd5-113">**ColorHLSToRGB**</span><span class="sxs-lookup"><span data-stu-id="d3cd5-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="d3cd5-114">Convertit les couleurs de teinte-luminance-saturation (TLS) au format RVB.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="d3cd5-115">**ColorRGBToHLS**</span><span class="sxs-lookup"><span data-stu-id="d3cd5-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="d3cd5-116">Convertit les couleurs RVB en format de saturation de la teinte (TSL).</span><span class="sxs-lookup"><span data-stu-id="d3cd5-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="d3cd5-117">**SHCreateShellPalette**</span><span class="sxs-lookup"><span data-stu-id="d3cd5-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="d3cd5-118">Crée une palette de demi-teintes pour le contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="d3cd5-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




