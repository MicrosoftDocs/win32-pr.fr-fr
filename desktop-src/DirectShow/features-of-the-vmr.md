---
description: Fonctionnalités de VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Fonctionnalités de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516161"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="ae78a-103">Fonctionnalités de VMR</span><span class="sxs-lookup"><span data-stu-id="ae78a-103">Features of the VMR</span></span>

<span data-ttu-id="ae78a-104">Le convertisseur de mixage vidéo 7 (VMR-7) prend en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae78a-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="ae78a-105">Mélange réel de plusieurs flux vidéo à l’aide des fonctionnalités de fusion alpha des périphériques matériels Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ae78a-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="ae78a-106">La possibilité de brancher votre propre composant de composition pour implémenter des effets et des transitions entre plusieurs flux vidéo entrant VMR.</span><span class="sxs-lookup"><span data-stu-id="ae78a-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="ae78a-107">Rendu true sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ae78a-107">True windowless rendering.</span></span> <span data-ttu-id="ae78a-108">Il n’est plus nécessaire de faire de la fenêtre de lecture vidéo un enfant de la fenêtre de l’application afin de contenir la lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="ae78a-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="ae78a-109">Le nouveau mode de rendu sans fenêtre de VMR permet aux applications d’héberger facilement la lecture vidéo dans n’importe quelle fenêtre sans avoir à transférer les messages de fenêtre au convertisseur pour le traitement spécifique au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="ae78a-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="ae78a-110">Nouveau mode de lecture non rendu dans lequel les applications peuvent fournir leur propre composant allocateur pour accéder à l’image vidéo décodée avant de l’afficher à l’écran.</span><span class="sxs-lookup"><span data-stu-id="ae78a-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="ae78a-111">Prise en charge améliorée des PC équipés de plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="ae78a-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="ae78a-112">Prise en charge de la nouvelle architecture d’accélération vidéo DirectX de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae78a-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="ae78a-113">Prise en charge de la lecture vidéo de haute qualité simultanément sur plusieurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="ae78a-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="ae78a-114">Prise en charge du mode exclusif DirectDraw</span><span class="sxs-lookup"><span data-stu-id="ae78a-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="ae78a-115">100% de compatibilité descendante avec les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="ae78a-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="ae78a-116">Prise en charge du pas à pas et d’un moyen fiable de capturer l’image actuelle affichée.</span><span class="sxs-lookup"><span data-stu-id="ae78a-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="ae78a-117">La possibilité pour les applications de se mélanger facilement à l’aide d’alpha de leurs propres données d’image statiques (telles que les logos de canaux ou les composants d’interface utilisateur) avec la vidéo de façon sans scintillement.</span><span class="sxs-lookup"><span data-stu-id="ae78a-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="ae78a-118">VMR-9 prend en charge toutes les fonctionnalités mentionnées ci-dessus, ainsi que :</span><span class="sxs-lookup"><span data-stu-id="ae78a-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="ae78a-119">La possibilité de traiter les données vidéo directement avec les API Direct3D, telles que les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae78a-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="ae78a-120">Prise en charge améliorée du contenu vidéo entrelacé.</span><span class="sxs-lookup"><span data-stu-id="ae78a-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="ae78a-121">Prise en charge sur toutes les plateformes prises en charge par DirectX.</span><span class="sxs-lookup"><span data-stu-id="ae78a-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae78a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae78a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae78a-123">À propos du rendu de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="ae78a-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



