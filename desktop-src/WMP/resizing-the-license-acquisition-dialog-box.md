---
title: Redimensionnement de la boîte de dialogue acquisition de licence
description: Redimensionnement de la boîte de dialogue acquisition de licence
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Lecteur Windows Media, boîte de dialogue redimensionner l’acquisition de licence
- Lecteur Windows Media, boîte de dialogue acquisition de licence
- Lecteur Windows Media, attribut DRM_LicenseAcqURL
- boîte de dialogue Redimensionnement d’acquisition de licence
- Boîte de dialogue acquisition de licence
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380142"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="ff734-109">Redimensionnement de la boîte de dialogue acquisition de licence</span><span class="sxs-lookup"><span data-stu-id="ff734-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="ff734-110">Vous pouvez ajouter des paramètres de chaîne de requête à l’URL que vous fournissez pour l’attribut **DRM \_ LicenseAcqURL** afin de spécifier une taille pour la boîte de dialogue acquisition de licence Windows Media Player 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff734-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="ff734-111">Le tableau suivant répertorie les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ff734-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="ff734-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ff734-112">Parameter</span></span> | <span data-ttu-id="ff734-113">Description</span><span class="sxs-lookup"><span data-stu-id="ff734-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="ff734-114">*DlgX*</span><span class="sxs-lookup"><span data-stu-id="ff734-114">*DlgX*</span></span>    | <span data-ttu-id="ff734-115">Spécifie la largeur de la boîte de dialogue, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ff734-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="ff734-116">*DlgY*</span><span class="sxs-lookup"><span data-stu-id="ff734-116">*DlgY*</span></span>    | <span data-ttu-id="ff734-117">Spécifie la hauteur, en pixels, de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ff734-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="ff734-118">Par exemple, l’URL d’acquisition de licence suivante entraînerait l’ouverture de la boîte de dialogue acquisition de licence avec une taille de 800 x 600 pixels :</span><span class="sxs-lookup"><span data-stu-id="ff734-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="ff734-119">La taille maximale de la boîte de dialogue ne dépasse jamais les dimensions actuelles de l’écran moins de 20 pixels.</span><span class="sxs-lookup"><span data-stu-id="ff734-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="ff734-120">La taille minimale est de 333 x 210 pixels (taille par défaut).</span><span class="sxs-lookup"><span data-stu-id="ff734-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="ff734-121">Cette fonctionnalité nécessite le lecteur Windows Media 10 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff734-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff734-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff734-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff734-123">**Lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ff734-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




