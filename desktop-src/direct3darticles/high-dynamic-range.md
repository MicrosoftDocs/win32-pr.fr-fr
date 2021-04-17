---
title: Utilisation de DirectX avec des écrans à haute gamme dynamique et une couleur avancée
description: Cette rubrique fournit une vue d’ensemble technique du rendu de contenu Direct3D 11 et Direct3D 12 à plage dynamique élevée dans un affichage HDR10 à l’aide de la prise en charge avancée des couleurs Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104571637"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="acacc-103">Utilisation de DirectX avec des affichages de plage dynamique élevée et une couleur avancée</span><span class="sxs-lookup"><span data-stu-id="acacc-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="acacc-104">Cette rubrique fournit une vue d’ensemble technique de la génération de contenu Direct3D 11 et Direct3D 12 de gamme dynamique élevée (HDR) dans un affichage HDR10 à l’aide de la prise en charge avancée des couleurs Windows 10.</span><span class="sxs-lookup"><span data-stu-id="acacc-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="acacc-105">Elle résume les principales différences conceptuelles entre la génération de l’affichage HDR10 et les affichages de la plage dynamique standard (SDR).</span><span class="sxs-lookup"><span data-stu-id="acacc-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="acacc-106">Il aborde également les principales exigences techniques de votre application pour prendre en charge correctement Windows Advanced Color, ainsi que les recommandations et les meilleures pratiques.</span><span class="sxs-lookup"><span data-stu-id="acacc-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="acacc-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="acacc-107">Introduction</span></span>

<span data-ttu-id="acacc-108">Windows 10 prend en charge les affichages HDR et autres couleurs avancées, ce qui offre une fidélité des couleurs nettement supérieure à celle des affichages SDR traditionnels.</span><span class="sxs-lookup"><span data-stu-id="acacc-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="acacc-109">Vous pouvez utiliser Direct3D, Direct2D et d’autres API graphiques pour afficher le contenu HDR sur un affichage de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="acacc-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="acacc-110">Couleurs avancées de Windows fait référence à plusieurs technologies connexes, introduites dans la version 1703 de Windows 10, qui assurent la prise en charge des affichages qui dépassent les capacités de couleur des affichages de plage dynamique standard (SDR) classiques.</span><span class="sxs-lookup"><span data-stu-id="acacc-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="acacc-111">Les trois principales fonctionnalités étendues sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="acacc-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="acacc-112">Le type le plus courant d’affichage des couleurs avancées, HDR10, prend en charge les trois fonctionnalités étendues.</span><span class="sxs-lookup"><span data-stu-id="acacc-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="acacc-113">Plage dynamique élevée</span><span class="sxs-lookup"><span data-stu-id="acacc-113">High dynamic range</span></span>

<span data-ttu-id="acacc-114">La plage dynamique fait référence à la différence entre la luminance maximale et minimale dans une scène. Cela est souvent mesuré en nits (candelas par centimètre carré).</span><span class="sxs-lookup"><span data-stu-id="acacc-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="acacc-115">Des scènes réalistes, telles que ce coucher de soleil, ont souvent des plages dynamiques de 10 commandes de luminance. l’oeil humain peut discerner une plage encore plus grande après l’adaptation.</span><span class="sxs-lookup"><span data-stu-id="acacc-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![image d’un soleil avec la luminosité et les points les plus sombres dans la scène étiquetée](images/HDR-HDR.jpg)

<span data-ttu-id="acacc-117">Depuis Direct3D 9, les moteurs graphiques ont été en mesure de rendre leurs scènes en interne avec ce niveau de fidélité physique.</span><span class="sxs-lookup"><span data-stu-id="acacc-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="acacc-118">Toutefois, un affichage de plage dynamique standard standard peut reproduire uniquement un petit nombre de commandes de luminance, et par conséquent, tout contenu à affichage HDR devait être Tonemapped (compressé) dans la plage limitée de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="acacc-119">Les nouveaux affichages HDR, y compris ceux qui sont conformes à la norme HDR10 (BT. 2100), franchissent cette limitation.</span><span class="sxs-lookup"><span data-stu-id="acacc-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="acacc-120">Gamme de couleurs larges avec gestion automatique des couleurs du système</span><span class="sxs-lookup"><span data-stu-id="acacc-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="acacc-121">La gamme de couleurs fait référence à la plage et à la saturation des teintes qu’un affichage peut reproduire.</span><span class="sxs-lookup"><span data-stu-id="acacc-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="acacc-122">La couleur naturelle la plus saturée que l’oeil humain peut percevoir est un éclairage monochromatique pur, tel que celui produit par un laser.</span><span class="sxs-lookup"><span data-stu-id="acacc-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="acacc-123">Toutefois, l’affichage du grand public peut souvent reproduire des couleurs uniquement dans la gamme sRVB, ce qui représente seulement environ 35% de toutes les couleurs perceptibles par l’homme.</span><span class="sxs-lookup"><span data-stu-id="acacc-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="acacc-124">Le diagramme ci-dessous est une représentation du « locus spectral » humain, ou de toutes les couleurs perceptibles (à un niveau de luminance donné), où le plus petit triangle est la gamme sRVB.</span><span class="sxs-lookup"><span data-stu-id="acacc-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![diagramme du locus spectral humain et de la gamme de couleurs sRVB](images/HDR-WCG.jpg)

<span data-ttu-id="acacc-126">Haut de gamme, les PC professionnels affichent des gammes de couleurs de longue durée qui sont beaucoup plus larges que l’sRVB, comme Adobe RGB et D65-P3.</span><span class="sxs-lookup"><span data-stu-id="acacc-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="acacc-127">Et ces affichages à large gamme deviennent de plus en plus courants.</span><span class="sxs-lookup"><span data-stu-id="acacc-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="acacc-128">Toutefois, avant la couleur avancée, Windows n’effectuait aucune gestion des couleurs au niveau du système pour les applications.</span><span class="sxs-lookup"><span data-stu-id="acacc-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="acacc-129">Cela signifiait que si une application DirectX affichait, par exemple, une couleur rouge ou RVB pure (1,0, 0,0, 0,0) à sa chaîne de permutation, Windows analyserait simplement le rouge le plus saturé que l’affichage pouvait reproduire, quelle que soit la gamme de couleurs réelle de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="acacc-130">Les applications qui nécessitaient une haute précision des couleurs peuvent interroger les fonctionnalités de couleur de l’affichage (par exemple, à l’aide de profils ICC) et effectuer leur propre gestion des couleurs in-process pour cibler correctement la gamme de couleurs de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="acacc-131">Toutefois, la grande majorité des applications et du contenu visuel suppose que l’affichage est sRVB et qu’ils s’appuient sur le système d’exploitation pour respecter cette hypothèse.</span><span class="sxs-lookup"><span data-stu-id="acacc-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="acacc-132">Couleurs avancées de Windows ajoute la gestion automatique des couleurs au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="acacc-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="acacc-133">Le Gestionnaire de fenêtrage (DWM) est le compositeur de Windows.</span><span class="sxs-lookup"><span data-stu-id="acacc-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="acacc-134">Quand la couleur avancée est activée, le DWM effectue une conversion de couleur explicite du colorspace du contenu visuel de l’application vers un espace de couleurs de composition canonique, qui est ScRVB.</span><span class="sxs-lookup"><span data-stu-id="acacc-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="acacc-135">Windows convertit ensuite les couleurs du contenu trame composé en espace de couleurs natif de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="acacc-136">De cette façon, le contenu sRGB traditionnel obtient automatiquement un comportement précis des couleurs, tandis que les applications avancées prenant en compte les couleurs peuvent tirer parti des fonctionnalités de couleur complètes de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="acacc-137">Précision profonde/profondeur de bit</span><span class="sxs-lookup"><span data-stu-id="acacc-137">Deep precision/bit depth</span></span>

<span data-ttu-id="acacc-138">La précision numérique, ou profondeur de bits, fait référence à la représentation ou à la distinction entre des couleurs similaires mais distinctes sans bandes ni artefacts.</span><span class="sxs-lookup"><span data-stu-id="acacc-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="acacc-139">Le PC grand public affiche la prise en charge de 8 bits par canal de couleur, tandis que l’œil humain requiert au moins 10-12 bits de précision pour éviter les distorsions perceptibles, sans recourir à des techniques telles que le tramage ou en fonction des conditions d’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![image des moulins à une simulation de 2 bits par canal de couleur par rapport à 8 bits par canal](images/HDR-bitdepth.jpg)

<span data-ttu-id="acacc-141">Avant la couleur avancée, le DWM limite les applications Windows à la sortie du contenu à 8 bits seulement par canal de couleur, même si l’affichage prenait en charge une profondeur de bits supérieure.</span><span class="sxs-lookup"><span data-stu-id="acacc-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="acacc-142">Quand la couleur avancée est activée, le DWM effectue sa composition à l’aide du point à virgule flottante demi-précision IEEE (FP16), éliminant les goulots d’étranglement et permettant d’utiliser la précision totale de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="acacc-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acacc-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="acacc-144">Système d’exploitation (OS)</span><span class="sxs-lookup"><span data-stu-id="acacc-144">Operating system (OS)</span></span>

<span data-ttu-id="acacc-145">La prise en charge des couleurs avancées est tout d’abord fournie avec Windows 10, version 1703, et a été considérablement améliorée avec chaque mise à jour.</span><span class="sxs-lookup"><span data-stu-id="acacc-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="acacc-146">Cette rubrique suppose que votre application cible Windows 10, version 1903 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="acacc-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="acacc-147">Afficher</span><span class="sxs-lookup"><span data-stu-id="acacc-147">Display</span></span>

<span data-ttu-id="acacc-148">Pour tirer parti d’une plage dynamique élevée, vous devez disposer d’un affichage qui prend en charge la norme HDR10.</span><span class="sxs-lookup"><span data-stu-id="acacc-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="acacc-149">Windows fonctionne mieux avec les affichages qui sont [certifiés VESA DisplayHDR](https://displayhdr.org/).</span><span class="sxs-lookup"><span data-stu-id="acacc-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="acacc-150">Processeur graphique (GPU)</span><span class="sxs-lookup"><span data-stu-id="acacc-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="acacc-151">Un GPU récent est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="acacc-151">A recent GPU is required.</span></span> <span data-ttu-id="acacc-152">Pour prendre en charge les affichages HDR10, Windows 10 requiert l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="acacc-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="acacc-153">NVIDIA GeForce 1000 Series (Pascal) ou plus récent</span><span class="sxs-lookup"><span data-stu-id="acacc-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="acacc-154">AMD Radeon RX 400 Series (Polaris) ou plus récent</span><span class="sxs-lookup"><span data-stu-id="acacc-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="acacc-155">Gamme Intel Core 7 sélectionnée (Kaby Lake) ou plus récente</span><span class="sxs-lookup"><span data-stu-id="acacc-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="acacc-156">Notez que des exigences matérielles supplémentaires s’appliquent en fonction des scénarios, y compris l’accélération du codec matériel (10 bits HEVC, 10 bits VP9, etc.) et la prise en charge de PlayReady (SL3000).</span><span class="sxs-lookup"><span data-stu-id="acacc-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="acacc-157">Contactez le fournisseur de votre GPU pour obtenir des informations plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="acacc-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="acacc-158">Pilote Graphics (WDDM)</span><span class="sxs-lookup"><span data-stu-id="acacc-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="acacc-159">Le dernier pilote graphique disponible est vivement recommandé, soit à partir de Windows Update, soit à partir du site Web du fabricant du GPU ou du PC.</span><span class="sxs-lookup"><span data-stu-id="acacc-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="acacc-160">Pour Windows 10, version 1903 et versions ultérieures, nous recommandons des pilotes qui prennent en charge au moins Windows Display Driver Model (WDDM) version 2,6.</span><span class="sxs-lookup"><span data-stu-id="acacc-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="acacc-161">API de rendu prises en charge</span><span class="sxs-lookup"><span data-stu-id="acacc-161">Supported rendering APIs</span></span>

<span data-ttu-id="acacc-162">Windows 10 prend en charge un large éventail d’API et d’infrastructures de rendu.</span><span class="sxs-lookup"><span data-stu-id="acacc-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="acacc-163">La prise en charge avancée des couleurs repose fondamentalement sur votre application capable d’effectuer une présentation moderne à l’aide de DXGI ou des API de la couche visuelle.</span><span class="sxs-lookup"><span data-stu-id="acacc-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="acacc-164">Infrastructure DirectX Graphics (DXGI)</span><span class="sxs-lookup"><span data-stu-id="acacc-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="acacc-165">Couche visuelle (Windows. UI. composition)</span><span class="sxs-lookup"><span data-stu-id="acacc-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="acacc-166">Par conséquent, toute API de rendu pouvant être sortie vers l’une de ces méthodes de présentation peut prendre en charge la couleur avancée.</span><span class="sxs-lookup"><span data-stu-id="acacc-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="acacc-167">Cela comprend, mais n’est pas limité à ces.</span><span class="sxs-lookup"><span data-stu-id="acacc-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="acacc-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="acacc-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="acacc-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="acacc-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="acacc-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="acacc-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="acacc-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="acacc-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="acacc-172">Requiert l’utilisation des API **CanvasSwapChain** ou **CanvasSwapChainPanel** de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="acacc-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="acacc-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="acacc-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="acacc-174">Prend en charge le rendu d’encre sèche personnalisé à l’aide de DirectX.</span><span class="sxs-lookup"><span data-stu-id="acacc-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="acacc-175">XAML</span><span class="sxs-lookup"><span data-stu-id="acacc-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="acacc-176">Prend en charge la lecture des vidéos HDR à l’aide de **MediaPlayerElement**.</span><span class="sxs-lookup"><span data-stu-id="acacc-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="acacc-177">Prend en charge le décodage des images JPEG XR à l’aide de l’élément **image** .</span><span class="sxs-lookup"><span data-stu-id="acacc-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="acacc-178">Prend en charge l’interopérabilité DirectX à l’aide de **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="acacc-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="acacc-179">Gestion des fonctionnalités d’affichage dynamiques</span><span class="sxs-lookup"><span data-stu-id="acacc-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="acacc-180">Windows 10 prend en charge un large éventail d’affichages de couleurs avancés, allant des panneaux intégrés à l’efficacité énergétique aux moniteurs de jeux et téléviseurs haut de gamme.</span><span class="sxs-lookup"><span data-stu-id="acacc-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="acacc-181">Les utilisateurs Windows s’attendent à ce que votre application gère en toute transparence toutes ces variations, y compris les affichages SDR existants.</span><span class="sxs-lookup"><span data-stu-id="acacc-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="acacc-182">Windows 10 permet à l’utilisateur de contrôler les fonctionnalités HDR et Advanced Color.</span><span class="sxs-lookup"><span data-stu-id="acacc-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="acacc-183">Votre application doit détecter la configuration de l’affichage actuel et répondre de manière dynamique à toute modification apportée à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="acacc-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="acacc-184">Cela peut se produire pour de nombreuses raisons, par exemple parce que l’utilisateur a activé ou désactivé une fonctionnalité, ou a déplacé l’application entre différents affichages ou que l’état d’alimentation du système a changé.</span><span class="sxs-lookup"><span data-stu-id="acacc-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="acacc-185">Applications plateforme Windows universelle (UWP)</span><span class="sxs-lookup"><span data-stu-id="acacc-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="acacc-186">Si vous écrivez une application UWP, quelle que soit l’API de rendu graphique que vous utilisez, utilisez [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) pour obtenir les fonctionnalités d’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="acacc-187">Obtenez une instance de **AdvancedColorInfo** à partir de [**DisplayInformation :: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span><span class="sxs-lookup"><span data-stu-id="acacc-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="acacc-188">Pour vérifier le type de couleurs avancé actuellement actif, utilisez la propriété [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) .</span><span class="sxs-lookup"><span data-stu-id="acacc-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="acacc-189">Dans Windows 10, version 1903 et versions ultérieures, cette méthode retourne l’une des trois valeurs possibles : **SDR**, **WCG** ou **HDR**.</span><span class="sxs-lookup"><span data-stu-id="acacc-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="acacc-190">Il s’agit de la propriété la plus importante à vérifier, et vous devez configurer votre pipeline de rendu et de présentation en réponse au genre actif.</span><span class="sxs-lookup"><span data-stu-id="acacc-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="acacc-191">Pour vérifier les types de couleurs avancés pris en charge, mais pas nécessairement actifs, appelez [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span><span class="sxs-lookup"><span data-stu-id="acacc-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="acacc-192">Vous pouvez utiliser ces informations, par exemple, pour inviter l’utilisateur à accéder à l’application Paramètres Windows afin qu’il puisse activer HDR ou WCG.</span><span class="sxs-lookup"><span data-stu-id="acacc-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="acacc-193">Les autres membres de **AdvancedColorInfo** fournissent des informations quantitatives sur le volume de couleurs physiques du panneau (luminance et chrominance), correspondant aux métadonnées HDR statiques 2086.</span><span class="sxs-lookup"><span data-stu-id="acacc-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="acacc-194">Utilisez ces informations pour configurer le mappage HDR tonemapping et de gammes de votre application.</span><span class="sxs-lookup"><span data-stu-id="acacc-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="acacc-195">Pour gérer les modifications apportées aux fonctionnalités de couleur avancées, inscrivez-vous à l’événement [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) .</span><span class="sxs-lookup"><span data-stu-id="acacc-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="acacc-196">Cet événement est déclenché si un paramètre des fonctionnalités de couleur avancées de l’affichage change pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="acacc-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="acacc-197">Gérez cet événement en obtenant une nouvelle instance de **AdvancedColorInfo** et en vérifiant les valeurs qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="acacc-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="acacc-198">Applications DirectX Desktop (Win32)</span><span class="sxs-lookup"><span data-stu-id="acacc-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="acacc-199">Si vous écrivez une application Win32 et utilisez DirectX pour effectuer le rendu, utilisez [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) pour obtenir des fonctionnalités d’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="acacc-200">Obtenez une instance de ce struct via [**IDXGIOutput6 :: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span><span class="sxs-lookup"><span data-stu-id="acacc-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="acacc-201">Pour vérifier le type de couleurs avancé actuellement actif, utilisez la propriété **ColorSpace** , qui est de type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), et contient l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="acacc-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="acacc-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="acacc-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="acacc-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="acacc-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="acacc-204">D’autres types de couleurs avancés, tels que WCG, sont traités comme SDR par DXGI.</span><span class="sxs-lookup"><span data-stu-id="acacc-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="acacc-205">Vous ne pouvez pas utiliser DXGI pour identifier un affichage WCG.</span><span class="sxs-lookup"><span data-stu-id="acacc-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="acacc-206">DXGI ne vous permet pas de vérifier les types de couleurs avancés qui sont pris en charge, mais qui ne sont pas actifs pour le moment.</span><span class="sxs-lookup"><span data-stu-id="acacc-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="acacc-207">La plupart des autres membres de **DXGI_OUTPUT_DESC1** fournissent des informations quantitatives sur le volume de couleurs physiques du panneau (luminance et chrominance), correspondant aux métadonnées HDR statiques 2086.</span><span class="sxs-lookup"><span data-stu-id="acacc-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="acacc-208">Utilisez ces informations pour configurer le mappage HDR tonemapping et de gammes de votre application.</span><span class="sxs-lookup"><span data-stu-id="acacc-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="acacc-209">Les applications Win32 n’ont pas de mécanisme natif pour répondre aux modifications de capacité de couleurs avancées.</span><span class="sxs-lookup"><span data-stu-id="acacc-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="acacc-210">Au lieu de cela, si votre application utilise une boucle de rendu, vous devez interroger [**IDXGIFactory1 :: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) avec chaque frame.</span><span class="sxs-lookup"><span data-stu-id="acacc-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="acacc-211">Si elle indique **false**, vous devez obtenir un nouveau **DXGI_OUTPUT_DESC1** et vérifier les valeurs qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="acacc-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="acacc-212">En outre, votre pompe de messages Win32 doit gérer le [**WM_SIZE**](../winmsg/wm-size.md) message, ce qui indique que votre application peut avoir été déplacée entre différents affichages.</span><span class="sxs-lookup"><span data-stu-id="acacc-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="acacc-213">Pour obtenir une nouvelle **DXGI_OUTPUT_DESC1**, vous devez obtenir l’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="acacc-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="acacc-214">Toutefois, vous ne devez pas appeler **IDXGISwapChain :: GetContainingOutput**.</span><span class="sxs-lookup"><span data-stu-id="acacc-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="acacc-215">Cela est dû au fait que les chaînes de permutation retournent une sortie DXGI obsolète une fois que **DXGIFactory :: IsCurrent** a la valeur false et que la recréation de la chaîne de permutation pour obtenir une sortie actuelle se traduit par un écran noir temporaire.</span><span class="sxs-lookup"><span data-stu-id="acacc-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="acacc-216">Au lieu de cela, nous vous recommandons d’énumérer les limites de toutes les sorties DXGI et de déterminer celle qui a le plus d’intersection avec les limites de la fenêtre de votre application.</span><span class="sxs-lookup"><span data-stu-id="acacc-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="acacc-217">L’exemple de code suivant provient du [référentiel DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="acacc-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="acacc-218">Configuration de votre chaîne d’échange DirectX</span><span class="sxs-lookup"><span data-stu-id="acacc-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="acacc-219">Une fois que vous avez déterminé que l’affichage prend actuellement en charge les fonctionnalités de couleur avancées, configurez votre chaîne de permutation comme suit.</span><span class="sxs-lookup"><span data-stu-id="acacc-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="acacc-220">Utiliser un effet de rotation du modèle de présentation</span><span class="sxs-lookup"><span data-stu-id="acacc-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="acacc-221">Lors de la création de votre chaîne de permutation à l’aide de **CreateSwapChainFor [HWND | Composition | CoreWindow]** , vous devez utiliser le modèle de retournement dxgi en sélectionnant l’option **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ou **DXGI_SWAP_EFFECT_FLIP_DISCARD** , ce qui rend votre chaîne de permutation éligible pour le traitement des couleurs avancé à partir de DWM et diverses optimisations en plein écran.</span><span class="sxs-lookup"><span data-stu-id="acacc-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="acacc-222">Pour plus d’informations, reportez-vous à la rubrique [pour obtenir des performances optimales, utiliser dxgi Flip Model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="acacc-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="acacc-223">Option 1.</span><span class="sxs-lookup"><span data-stu-id="acacc-223">Option 1.</span></span> <span data-ttu-id="acacc-224">Utiliser le format de pixel FP16 et l’espace de couleurs ScRVB</span><span class="sxs-lookup"><span data-stu-id="acacc-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="acacc-225">Windows 10 prend en charge deux combinaisons principales du format de pixel et de l’espace colorimétrique pour la couleur avancée.</span><span class="sxs-lookup"><span data-stu-id="acacc-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="acacc-226">Sélectionnez-en un en fonction des exigences spécifiques de votre application.</span><span class="sxs-lookup"><span data-stu-id="acacc-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="acacc-227">Pour les applications à usage général, lors de la création de votre chaîne de permutation, nous vous recommandons de spécifier [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="acacc-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="acacc-228">C’est ce que l’on appelle également *FP16* dans votre [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="acacc-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="acacc-229">Par défaut, une chaîne de permutation créée avec un format de pixel à virgule flottante est traitée comme si elle utilise l’espace de couleurs [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , également appelé *ScRVB*.</span><span class="sxs-lookup"><span data-stu-id="acacc-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="acacc-230">Cette combinaison vous fournit la plage numérique et la précision pour spécifier presque toutes les couleurs physiquement possibles et effectuer un traitement arbitraire, y compris une fusion.</span><span class="sxs-lookup"><span data-stu-id="acacc-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="acacc-231">En outre, si vous utilisez Direct2D, Win2D ou Windows. UI. composition, il s’agit de la seule combinaison prise en charge pour toute chaîne de permutation ou cible intermédiaire qui contient du contenu de couleur avancé.</span><span class="sxs-lookup"><span data-stu-id="acacc-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="acacc-232">Le principal inconvénient de cette option est qu’elle consomme 64 bits par pixel, ce qui double la bande passante du GPU et la consommation de mémoire par rapport aux formats de pixel de la base de SDR.</span><span class="sxs-lookup"><span data-stu-id="acacc-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="acacc-233">En outre, ScRVB utilise des valeurs numériques qui se trouvent en dehors de la plage normalisée [0, 1] pour représenter les couleurs qui sont en dehors de la gamme sRVB et/ou supérieures à 80 nits de luminance.</span><span class="sxs-lookup"><span data-stu-id="acacc-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="acacc-234">Par exemple, ScRVB (1,0, 1,0, 1,0) encode le blanc D65 standard à 80 nits ; Toutefois, ScRVB (12,5, 12,5, 12,5) encode le même blanc D65 à une plus grande luminosité de 1000 nits.</span><span class="sxs-lookup"><span data-stu-id="acacc-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="acacc-235">Certaines opérations graphiques nécessitent une plage numérique normalisée et vous devez soit modifier l’opération, soit renormaliser les valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="acacc-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="acacc-236">Option 2 : utiliser le format de pixel UINT10/RGB10 et l’espace de couleurs HDR10/BT. 2100</span><span class="sxs-lookup"><span data-stu-id="acacc-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="acacc-237">Pour les applications qui consomment du contenu encodé HDR10, tels que des lecteurs multimédias ou des applications qui doivent être utilisés principalement dans des scénarios en plein écran tels que des jeux, lors de la création de votre chaîne de permutation, vous devez envisager de spécifier [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) dans [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="acacc-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="acacc-238">Par défaut, il est traité comme utilisant l’espace de couleurs sRVB. par conséquent, vous devez appeler explicitement [**IDXGISwapChain3 :: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)et définir comme espace de couleurs [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), également appelé HDR10/BT. 2100.</span><span class="sxs-lookup"><span data-stu-id="acacc-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="acacc-239">Cette combinaison présente des restrictions plus strictes que FP16.</span><span class="sxs-lookup"><span data-stu-id="acacc-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="acacc-240">Vous pouvez l’utiliser uniquement avec Direct3D 11 ou Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="acacc-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="acacc-241">En outre, UINT10/HDR10 présente des limitations sous la forme d’un format intermédiaire, car il utilise la fonction ST. 084 EOTF (fonction « gamma »), qui est très non linéaire et optimisée comme format câble, et parce qu’il n’offre que 2 bits d’alpha.</span><span class="sxs-lookup"><span data-stu-id="acacc-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="acacc-242">Toutefois, cette combinaison peut offrir des optimisations de performances puissantes lorsqu’elle est utilisée dans la sortie finale de votre application.</span><span class="sxs-lookup"><span data-stu-id="acacc-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="acacc-243">Il consomme les mêmes 32 bits par pixel que les formats de pixel de l’SDR UINT8 traditionnels.</span><span class="sxs-lookup"><span data-stu-id="acacc-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="acacc-244">En outre, dans certains scénarios en plein écran, le système d’exploitation peut optimiser les performances en analysant directement la surface HDR10.</span><span class="sxs-lookup"><span data-stu-id="acacc-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="acacc-245">Utilisation d’une chaîne d’échange de couleurs avancée lorsque l’affichage est en mode SDR</span><span class="sxs-lookup"><span data-stu-id="acacc-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="acacc-246">Vous pouvez utiliser une chaîne d’échange de couleurs avancée même si l’affichage ne prend pas en charge une partie ou la totalité des fonctionnalités de couleur avancées requises par votre contenu.</span><span class="sxs-lookup"><span data-stu-id="acacc-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="acacc-247">Dans ce cas, le Gestionnaire de fenêtrage (DWM) downconvert votre contenu pour l’adapter aux fonctionnalités de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="acacc-248">Dans Windows 10, version 1903 et versions ultérieures, le découpage numérique sera effectué. par exemple, si vous affichez une chaîne de permutation FP16 ScRVB, tout en dehors de la plage numérique [0, 1] est tronqué.</span><span class="sxs-lookup"><span data-stu-id="acacc-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="acacc-249">Ce comportement downconversion se produira également si votre fenêtre d’application chevauche plusieurs affichages avec des fonctionnalités de couleur avancées différentes.</span><span class="sxs-lookup"><span data-stu-id="acacc-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="acacc-250">**AdvancedColorInfo** et **IDXGIOutput6** sont abstraits pour signaler uniquement les caractéristiques de l’affichage « principal » (définies comme affichage contenant le centre de la fenêtre).</span><span class="sxs-lookup"><span data-stu-id="acacc-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="acacc-251">Restituer correctement le contenu SDR avec le niveau de référence SDR</span><span class="sxs-lookup"><span data-stu-id="acacc-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="acacc-252">Dans de nombreux scénarios, votre application souhaite afficher le contenu SDR et HDR. par exemple, le rendu des sous-titres ou des contrôles de transport sur une vidéo HDR ou une interface utilisateur dans une scène de jeu.</span><span class="sxs-lookup"><span data-stu-id="acacc-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="acacc-253">Il est important de comprendre le concept de *niveau de référence SDR* pour vous assurer que votre contenu SDR semble correct sur un affichage HDR.</span><span class="sxs-lookup"><span data-stu-id="acacc-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="acacc-254">Windows traite le contenu HDR comme étant _référencé par scène_, ce qui signifie qu’une valeur de couleur particulière doit être affichée à un niveau de luminance spécifique. par exemple, ScRVB (1,0, 1,0, 1,0) et HDR10 (497, 497, 497) encodent exactement D65 en blanc à 80 nits de luminance.</span><span class="sxs-lookup"><span data-stu-id="acacc-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="acacc-255">Pendant ce temps, le contenu SDR est traditionnellement soumis à la _sortie_ (ou à l’affichage), ce qui signifie que sa luminance est laissée à l’utilisateur ou à l’appareil ; par exemple, sRVB (1,0, 1,0, 1,0) encode le blanc D65 comme dans les exemples HDR, mais à toute luminance maximale pour laquelle l’affichage est configuré.</span><span class="sxs-lookup"><span data-stu-id="acacc-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="acacc-256">Windows permet à l’utilisateur d’ajuster le _niveau de référence SDR_ à sa préférence. Il s’agit de la luminance que Windows restituera sRVB (1,0, 1,0, 1,0) à.</span><span class="sxs-lookup"><span data-stu-id="acacc-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="acacc-257">Sur les moniteurs HDR de bureau, les niveaux de référence SDR sont généralement définis sur environ 200 nits.</span><span class="sxs-lookup"><span data-stu-id="acacc-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="acacc-258">Sur un écran qui prend en charge un contrôle de luminosité, par exemple sur un ordinateur portable, Windows ajuste également la luminance du contenu HDR (référencé par une scène) pour qu’il corresponde au niveau de luminosité souhaité de l’utilisateur, mais ce n’est pas visible pour l’application.</span><span class="sxs-lookup"><span data-stu-id="acacc-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="acacc-259">À moins que vous n’essayiez de garantir une reproduction exacte du signal HDR, vous pouvez généralement l’ignorer.</span><span class="sxs-lookup"><span data-stu-id="acacc-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="acacc-260">Si votre application affiche toujours les SDR et HDR pour séparer les surfaces et s’appuie sur la composition du système d’exploitation, Windows effectue automatiquement l’ajustement correct pour augmenter le contenu SDR au niveau de blanc souhaité.</span><span class="sxs-lookup"><span data-stu-id="acacc-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="acacc-261">Par exemple, si votre application utilise XAML et restitue le contenu HDR à son propre **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="acacc-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="acacc-262">Toutefois, si votre application effectue sa propre composition de contenu SDR et HDR en une seule surface, vous êtes chargé d’effectuer vous-même le réglage du niveau de référence SDR.</span><span class="sxs-lookup"><span data-stu-id="acacc-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="acacc-263">Sinon, le contenu SDR peut sembler trop sombre en supposant des conditions d’affichage de bureau typiques.</span><span class="sxs-lookup"><span data-stu-id="acacc-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="acacc-264">Tout d’abord, vous devez obtenir le niveau de référence SDR actuel, puis vous devez ajuster les valeurs de couleur de tout contenu SDR que vous rendez.</span><span class="sxs-lookup"><span data-stu-id="acacc-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="acacc-265">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="acacc-265">Step 1.</span></span> <span data-ttu-id="acacc-266">Obtenir le niveau de référence SDR actuel</span><span class="sxs-lookup"><span data-stu-id="acacc-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="acacc-267">Actuellement, seules les applications UWP peuvent obtenir le niveau de référence SDR actuel via [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span><span class="sxs-lookup"><span data-stu-id="acacc-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="acacc-268">Cette API requiert un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="acacc-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="acacc-269">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="acacc-269">Step 2.</span></span> <span data-ttu-id="acacc-270">Ajuster les valeurs de couleur du contenu SDR</span><span class="sxs-lookup"><span data-stu-id="acacc-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="acacc-271">Windows définit le niveau de référence nominal, ou par défaut, à 80 nits ; par conséquent, si vous deviez restituer un sRGB standard (1,0, 1,0, 1,0) blanc dans une chaîne de permutation FP16, il serait reproduit à une luminance de 80 nits.</span><span class="sxs-lookup"><span data-stu-id="acacc-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="acacc-272">Afin de faire correspondre le niveau de référence défini par l’utilisateur réel, vous devez ajuster le contenu SDR de 80 Nits au niveau spécifié via **AdvancedColorInfo. SdrWhiteLevelInNits**.</span><span class="sxs-lookup"><span data-stu-id="acacc-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="acacc-273">Si vous effectuez un rendu à l’aide de FP16 et ScRVB, ou de tout espace colorimétrique qui utilise le gamma linéaire (1,0), vous pouvez simplement multiplier la valeur de couleur SDR par _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_.</span><span class="sxs-lookup"><span data-stu-id="acacc-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="acacc-274">Si vous utilisez Direct2D, il existe une constante prédéfinie [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), qui a la valeur 80.</span><span class="sxs-lookup"><span data-stu-id="acacc-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="acacc-275">Si vous effectuez un rendu à l’aide d’un espace de couleurs gamma non linéaire tel que HDR10, le réglage du niveau de blanc SDR est plus complexe. Si vous écrivez votre propre nuanceur de pixels, vous devez envisager d’effectuer une conversion en gamma linéaire pour appliquer l’ajustement.</span><span class="sxs-lookup"><span data-stu-id="acacc-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="acacc-276">Adapter le contenu HDR aux fonctionnalités de l’affichage à l’aide de tonemapping</span><span class="sxs-lookup"><span data-stu-id="acacc-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="acacc-277">Les affichages couleur HDR et couleurs avancées varient considérablement en termes de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="acacc-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="acacc-278">Par exemple, la luminance minimale et maximale et la gamme de couleurs qu’elles peuvent reproduire.</span><span class="sxs-lookup"><span data-stu-id="acacc-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="acacc-279">Dans de nombreux cas, votre contenu HDR contient des couleurs qui dépassent les capacités de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="acacc-280">Pour une qualité d’image optimale, il est important que vous effectuiez des tonemapping HDR, en compressant essentiellement la plage de couleurs pour l’adapter à l’affichage tout en préservant l’objectif visuel du contenu.</span><span class="sxs-lookup"><span data-stu-id="acacc-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="acacc-281">Le paramètre unique le plus important à adapter à la luminance est Max, également appelé MaxCLL (niveau de lumière du contenu); les tonemappers plus sophistiquées vont également adapter les fonctions de luminance minimale (MinCLL) et/ou les couleurs primaires.</span><span class="sxs-lookup"><span data-stu-id="acacc-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="acacc-282">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="acacc-282">Step 1.</span></span> <span data-ttu-id="acacc-283">Obtenir les capacités de volume de couleurs de l’affichage</span><span class="sxs-lookup"><span data-stu-id="acacc-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="acacc-284">Applications plateforme Windows universelle (UWP)</span><span class="sxs-lookup"><span data-stu-id="acacc-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="acacc-285">Utilisez [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) pour obtenir le volume de couleurs de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="acacc-286">Applications DirectX Win32 (Desktop)</span><span class="sxs-lookup"><span data-stu-id="acacc-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="acacc-287">Utilisez [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) pour obtenir le volume de couleurs de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="acacc-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="acacc-288">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="acacc-288">Step 2.</span></span> <span data-ttu-id="acacc-289">Récupérer les informations sur les volumes de couleurs du contenu</span><span class="sxs-lookup"><span data-stu-id="acacc-289">Get the content's color volume information</span></span>

<span data-ttu-id="acacc-290">Selon l’origine de votre contenu HDR, il existe plusieurs façons possibles de déterminer sa luminance et les informations de la gamme de couleurs.</span><span class="sxs-lookup"><span data-stu-id="acacc-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="acacc-291">Certains fichiers vidéo et images HDR contiennent des métadonnées SMPTE ST. 2086.</span><span class="sxs-lookup"><span data-stu-id="acacc-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="acacc-292">Si votre contenu a été rendu dynamiquement, vous pourrez peut-être extraire des informations de scène à partir des étapes de rendu internes, par exemple la source de lumière la plus brillante dans une scène.</span><span class="sxs-lookup"><span data-stu-id="acacc-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="acacc-293">Une solution plus générale mais gourmande en calculs consiste à exécuter un histogramme ou une autre analyse sur le cadre rendu.</span><span class="sxs-lookup"><span data-stu-id="acacc-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="acacc-294">L' [exemple du kit de développement logiciel (SDK) des images de couleurs avancées de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) montre comment procéder à l’aide de Direct2D ; les extraits de code les plus pertinents sont inclus ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="acacc-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="acacc-295">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="acacc-295">Step 3.</span></span> <span data-ttu-id="acacc-296">Effectuer l’opération HDR tonemapping</span><span class="sxs-lookup"><span data-stu-id="acacc-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="acacc-297">Tonemapping est fondamentalement un processus de perte et peut être optimisé pour un certain nombre de mesures de perception ou objectives, donc il n’y a pas d’algorithme standard.</span><span class="sxs-lookup"><span data-stu-id="acacc-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="acacc-298">Windows fournit un [effet Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) intégré dans le cadre de Direct2D et dans le pipeline de lecture vidéo HDR Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acacc-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="acacc-299">Parmi les autres algorithmes couramment utilisés figurent les ACE cinématographiques, Reinhard et ITU-R BT. 2390-3 EETF (fonction de transfert électrique électrique).</span><span class="sxs-lookup"><span data-stu-id="acacc-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="acacc-300">Un opérateur Reinhard Tonemapper simplifié est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="acacc-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="acacc-301">Capture de contenu HDR et WCG</span><span class="sxs-lookup"><span data-stu-id="acacc-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="acacc-302">Les API qui prennent en charge la spécification des formats de pixel, tels que ceux de l’espace de noms [**Windows. Graphics. capture**](/uwp/api/windows.graphics.capture) et de la méthode [**IDXGIOutput5 ::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , permettent de capturer le contenu HDR et WCG sans perdre les informations sur les pixels.</span><span class="sxs-lookup"><span data-stu-id="acacc-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="acacc-303">Notez qu’après avoir acquis des trames de contenu, un traitement supplémentaire est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="acacc-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="acacc-304">Par exemple, le mappage de tonalité HDR-à-SDR (par exemple, capture de capture d’écran SDR pour le partage Internet) et l’enregistrement de contenu avec le format approprié (par exemple, JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="acacc-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acacc-305">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="acacc-305">Additional resources</span></span>

* <span data-ttu-id="acacc-306">*Utilisation du rendu HDR avec le kit d’outils DirectX* pour [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="acacc-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="acacc-307">Procédure pas à pas d’ajout de la prise en charge HDR à une application DirectX à l’aide du kit d’outils DirectX (DirectXTK).</span><span class="sxs-lookup"><span data-stu-id="acacc-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="acacc-308">[Exemple du kit de développement logiciel (SDK) couleurs avancées de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="acacc-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="acacc-309">Exemple SDK UWP mettant en œuvre une visionneuse d’images HDR et WCG avec prise en charge des couleurs avancées à l’aide de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="acacc-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="acacc-310">Illustre la gamme complète des meilleures pratiques pour les applications UWP, y compris la réponse aux modifications de capacité d’affichage et le réglage du niveau de blanc SDR.</span><span class="sxs-lookup"><span data-stu-id="acacc-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="acacc-311">[Exemple de bureau HDR Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="acacc-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="acacc-312">Exemple de SDK Desktop mettant en œuvre une scène HDR Direct3D 12 de base.</span><span class="sxs-lookup"><span data-stu-id="acacc-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="acacc-313">[Exemple UWP Direct3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="acacc-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="acacc-314">Équivalent UWP de l’exemple ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="acacc-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="acacc-315">[Exemple de PC Xbox ATG SimpleHDR](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="acacc-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="acacc-316">Exemple de SDK Desktop mettant en œuvre une scène HDR de base Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="acacc-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
