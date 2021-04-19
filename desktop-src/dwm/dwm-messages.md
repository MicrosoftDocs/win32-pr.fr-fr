---
title: Messages DWM
description: Cette section contient des informations sur les messages du Gestionnaire de fenêtrage (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Gestionnaire de fenêtrage (DWM), référence
- DWM (Gestionnaire de fenêtrage), référence
- Gestionnaire de fenêtrage (DWM), messages
- DWM (Gestionnaire de fenêtrage), messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106513701"
---
# <a name="dwm-messages"></a><span data-ttu-id="e2c98-107">Messages DWM</span><span class="sxs-lookup"><span data-stu-id="e2c98-107">DWM Messages</span></span>

<span data-ttu-id="e2c98-108">Cette section contient des informations sur les messages du Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="e2c98-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2c98-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e2c98-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2c98-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e2c98-110">Topic</span></span></th>
<th><span data-ttu-id="e2c98-111">Description</span><span class="sxs-lookup"><span data-stu-id="e2c98-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2c98-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-113">Informe toutes les fenêtres de niveau supérieur que la couleur de colorisation a changé.</span><span class="sxs-lookup"><span data-stu-id="e2c98-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2c98-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-115">Informe toutes les fenêtres de niveau supérieur que la composition DWM a été activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="e2c98-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e2c98-116">À compter de Windows 8, la composition DWM est toujours activée, ce qui signifie que ce message n’est pas envoyé, quelles que soient les modifications du mode vidéo.</span><span class="sxs-lookup"><span data-stu-id="e2c98-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2c98-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-118">Envoyé lorsque la stratégie de rendu de la zone non cliente a changé.</span><span class="sxs-lookup"><span data-stu-id="e2c98-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2c98-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-120">Indique à une fenêtre de fournir une image bitmap statique à utiliser comme <em>aperçu instantané</em> (également appelé aperçu de <em>lecture</em>) de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2c98-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2c98-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-122">Indique à une fenêtre de fournir une bitmap statique à utiliser comme représentation miniature de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2c98-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2c98-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2c98-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="e2c98-124">Envoyé lorsqu’une fenêtre décomposée DWM est agrandie.</span><span class="sxs-lookup"><span data-stu-id="e2c98-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





