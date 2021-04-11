---
description: Configuration système requise pour VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Configuration système requise pour VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203613"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="a5413-103">Configuration système requise pour VMR</span><span class="sxs-lookup"><span data-stu-id="a5413-103">VMR System Requirements</span></span>

<span data-ttu-id="a5413-104">VMR utilise exclusivement les capacités de traitement graphique de la carte graphique de l’ordinateur ; VMR n’effectue pas de fusion ou de rendu vidéo à l’aide du processeur hôte, car cela aurait un impact considérable sur la fréquence d’images et la qualité de la vidéo affichée.</span><span class="sxs-lookup"><span data-stu-id="a5413-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="a5413-105">En tirant parti des nouvelles fonctionnalités offertes par le VMR, notamment la fusion de plusieurs flux vidéo et/ou d’images d’application, les performances globales obtenues dépendent fortement des capacités de la carte graphique utilisée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5413-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="a5413-106">Les cartes graphiques qui fonctionnent correctement avec VMR intègrent la prise en charge matérielle suivante :</span><span class="sxs-lookup"><span data-stu-id="a5413-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="a5413-107">Prise en charge des surfaces YUV et « non-puissance de 2 ».</span><span class="sxs-lookup"><span data-stu-id="a5413-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="a5413-108">Capacité à StretchBlt des surfaces YUV à RVB DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="a5413-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="a5413-109">Au moins 16 Mo de mémoire vidéo si plusieurs flux vidéo doivent être mélangés ensemble.</span><span class="sxs-lookup"><span data-stu-id="a5413-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="a5413-110">La quantité réelle de mémoire requise dépend de la taille de l’image des flux vidéo et de la résolution du mode d’affichage utilisé.</span><span class="sxs-lookup"><span data-stu-id="a5413-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="a5413-111">Prise en charge d’une superposition RVB ou possibilité d’effectuer une fusion sur une surface de recouvrement YUV.</span><span class="sxs-lookup"><span data-stu-id="a5413-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="a5413-112">Décodage vidéo accélérée par le matériel (prise en charge du décodage DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="a5413-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="a5413-113">Taux de remplissage de pixels élevés.</span><span class="sxs-lookup"><span data-stu-id="a5413-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="a5413-114">VMR requiert la définition du moniteur système pour une profondeur de couleur d’au moins 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a5413-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="a5413-115">Le VMR ne peut pas être placé dans un état d’exécution si l’analyse est définie sur 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="a5413-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="a5413-116">En outre, certaines cartes vidéo ne peuvent pas effectuer d’opérations Direct3D lorsque l’affichage est défini sur 24 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="a5413-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a5413-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5413-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5413-118">À propos du rendu de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="a5413-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



