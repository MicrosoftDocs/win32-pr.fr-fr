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
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Utilisation de DirectX avec des affichages de plage dynamique élevée et une couleur avancée

Cette rubrique fournit une vue d’ensemble technique de la génération de contenu Direct3D 11 et Direct3D 12 de gamme dynamique élevée (HDR) dans un affichage HDR10 à l’aide de la prise en charge avancée des couleurs Windows 10. Elle résume les principales différences conceptuelles entre la génération de l’affichage HDR10 et les affichages de la plage dynamique standard (SDR). Il aborde également les principales exigences techniques de votre application pour prendre en charge correctement Windows Advanced Color, ainsi que les recommandations et les meilleures pratiques.

## <a name="introduction"></a>Introduction

Windows 10 prend en charge les affichages HDR et autres couleurs avancées, ce qui offre une fidélité des couleurs nettement supérieure à celle des affichages SDR traditionnels. Vous pouvez utiliser Direct3D, Direct2D et d’autres API graphiques pour afficher le contenu HDR sur un affichage de compatibilité.

Couleurs avancées de Windows fait référence à plusieurs technologies connexes, introduites dans la version 1703 de Windows 10, qui assurent la prise en charge des affichages qui dépassent les capacités de couleur des affichages de plage dynamique standard (SDR) classiques. Les trois principales fonctionnalités étendues sont décrites ci-dessous. Le type le plus courant d’affichage des couleurs avancées, HDR10, prend en charge les trois fonctionnalités étendues.

### <a name="high-dynamic-range"></a>Plage dynamique élevée

La plage dynamique fait référence à la différence entre la luminance maximale et minimale dans une scène. Cela est souvent mesuré en nits (candelas par centimètre carré). Des scènes réalistes, telles que ce coucher de soleil, ont souvent des plages dynamiques de 10 commandes de luminance. l’oeil humain peut discerner une plage encore plus grande après l’adaptation.

![image d’un soleil avec la luminosité et les points les plus sombres dans la scène étiquetée](images/HDR-HDR.jpg)

Depuis Direct3D 9, les moteurs graphiques ont été en mesure de rendre leurs scènes en interne avec ce niveau de fidélité physique. Toutefois, un affichage de plage dynamique standard standard peut reproduire uniquement un petit nombre de commandes de luminance, et par conséquent, tout contenu à affichage HDR devait être Tonemapped (compressé) dans la plage limitée de l’affichage. Les nouveaux affichages HDR, y compris ceux qui sont conformes à la norme HDR10 (BT. 2100), franchissent cette limitation.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Gamme de couleurs larges avec gestion automatique des couleurs du système

La gamme de couleurs fait référence à la plage et à la saturation des teintes qu’un affichage peut reproduire. La couleur naturelle la plus saturée que l’oeil humain peut percevoir est un éclairage monochromatique pur, tel que celui produit par un laser. Toutefois, l’affichage du grand public peut souvent reproduire des couleurs uniquement dans la gamme sRVB, ce qui représente seulement environ 35% de toutes les couleurs perceptibles par l’homme. Le diagramme ci-dessous est une représentation du « locus spectral » humain, ou de toutes les couleurs perceptibles (à un niveau de luminance donné), où le plus petit triangle est la gamme sRVB.

![diagramme du locus spectral humain et de la gamme de couleurs sRVB](images/HDR-WCG.jpg)

Haut de gamme, les PC professionnels affichent des gammes de couleurs de longue durée qui sont beaucoup plus larges que l’sRVB, comme Adobe RGB et D65-P3. Et ces affichages à large gamme deviennent de plus en plus courants. Toutefois, avant la couleur avancée, Windows n’effectuait aucune gestion des couleurs au niveau du système pour les applications. Cela signifiait que si une application DirectX affichait, par exemple, une couleur rouge ou RVB pure (1,0, 0,0, 0,0) à sa chaîne de permutation, Windows analyserait simplement le rouge le plus saturé que l’affichage pouvait reproduire, quelle que soit la gamme de couleurs réelle de l’affichage.

Les applications qui nécessitaient une haute précision des couleurs peuvent interroger les fonctionnalités de couleur de l’affichage (par exemple, à l’aide de profils ICC) et effectuer leur propre gestion des couleurs in-process pour cibler correctement la gamme de couleurs de l’affichage. Toutefois, la grande majorité des applications et du contenu visuel suppose que l’affichage est sRVB et qu’ils s’appuient sur le système d’exploitation pour respecter cette hypothèse.

Couleurs avancées de Windows ajoute la gestion automatique des couleurs au niveau du système. Le Gestionnaire de fenêtrage (DWM) est le compositeur de Windows. Quand la couleur avancée est activée, le DWM effectue une conversion de couleur explicite du colorspace du contenu visuel de l’application vers un espace de couleurs de composition canonique, qui est ScRVB. Windows convertit ensuite les couleurs du contenu trame composé en espace de couleurs natif de l’affichage. De cette façon, le contenu sRGB traditionnel obtient automatiquement un comportement précis des couleurs, tandis que les applications avancées prenant en compte les couleurs peuvent tirer parti des fonctionnalités de couleur complètes de l’affichage.

### <a name="deep-precisionbit-depth"></a>Précision profonde/profondeur de bit

La précision numérique, ou profondeur de bits, fait référence à la représentation ou à la distinction entre des couleurs similaires mais distinctes sans bandes ni artefacts. Le PC grand public affiche la prise en charge de 8 bits par canal de couleur, tandis que l’œil humain requiert au moins 10-12 bits de précision pour éviter les distorsions perceptibles, sans recourir à des techniques telles que le tramage ou en fonction des conditions d’affichage.

![image des moulins à une simulation de 2 bits par canal de couleur par rapport à 8 bits par canal](images/HDR-bitdepth.jpg)

Avant la couleur avancée, le DWM limite les applications Windows à la sortie du contenu à 8 bits seulement par canal de couleur, même si l’affichage prenait en charge une profondeur de bits supérieure. Quand la couleur avancée est activée, le DWM effectue sa composition à l’aide du point à virgule flottante demi-précision IEEE (FP16), éliminant les goulots d’étranglement et permettant d’utiliser la précision totale de l’affichage.

## <a name="system-requirements"></a>Configuration requise

### <a name="operating-system-os"></a>Système d’exploitation (OS)

La prise en charge des couleurs avancées est tout d’abord fournie avec Windows 10, version 1703, et a été considérablement améliorée avec chaque mise à jour. Cette rubrique suppose que votre application cible Windows 10, version 1903 ou ultérieure.

### <a name="display"></a>Afficher

Pour tirer parti d’une plage dynamique élevée, vous devez disposer d’un affichage qui prend en charge la norme HDR10. Windows fonctionne mieux avec les affichages qui sont [certifiés VESA DisplayHDR](https://displayhdr.org/).

### <a name="graphics-processor-gpu"></a>Processeur graphique (GPU)

Un GPU récent est nécessaire. Pour prendre en charge les affichages HDR10, Windows 10 requiert l’un des éléments suivants.

* NVIDIA GeForce 1000 Series (Pascal) ou plus récent
* AMD Radeon RX 400 Series (Polaris) ou plus récent
* Gamme Intel Core 7 sélectionnée (Kaby Lake) ou plus récente

Notez que des exigences matérielles supplémentaires s’appliquent en fonction des scénarios, y compris l’accélération du codec matériel (10 bits HEVC, 10 bits VP9, etc.) et la prise en charge de PlayReady (SL3000). Contactez le fournisseur de votre GPU pour obtenir des informations plus spécifiques.

### <a name="graphics-driver-wddm"></a>Pilote Graphics (WDDM)

Le dernier pilote graphique disponible est vivement recommandé, soit à partir de Windows Update, soit à partir du site Web du fabricant du GPU ou du PC. Pour Windows 10, version 1903 et versions ultérieures, nous recommandons des pilotes qui prennent en charge au moins Windows Display Driver Model (WDDM) version 2,6.

## <a name="supported-rendering-apis"></a>API de rendu prises en charge

Windows 10 prend en charge un large éventail d’API et d’infrastructures de rendu. La prise en charge avancée des couleurs repose fondamentalement sur votre application capable d’effectuer une présentation moderne à l’aide de DXGI ou des API de la couche visuelle.

* [Infrastructure DirectX Graphics (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Couche visuelle (Windows. UI. composition)](/windows/uwp/composition/visual-layer)

Par conséquent, toute API de rendu pouvant être sortie vers l’une de ces méthodes de présentation peut prendre en charge la couleur avancée. Cela comprend, mais n’est pas limité à ces.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Requiert l’utilisation des API **CanvasSwapChain** ou **CanvasSwapChainPanel** de niveau inférieur.
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Prend en charge le rendu d’encre sèche personnalisé à l’aide de DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Prend en charge la lecture des vidéos HDR à l’aide de **MediaPlayerElement**.
  * Prend en charge le décodage des images JPEG XR à l’aide de l’élément **image** .
  * Prend en charge l’interopérabilité DirectX à l’aide de **SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Gestion des fonctionnalités d’affichage dynamiques

Windows 10 prend en charge un large éventail d’affichages de couleurs avancés, allant des panneaux intégrés à l’efficacité énergétique aux moniteurs de jeux et téléviseurs haut de gamme. Les utilisateurs Windows s’attendent à ce que votre application gère en toute transparence toutes ces variations, y compris les affichages SDR existants.

Windows 10 permet à l’utilisateur de contrôler les fonctionnalités HDR et Advanced Color. Votre application doit détecter la configuration de l’affichage actuel et répondre de manière dynamique à toute modification apportée à la fonctionnalité. Cela peut se produire pour de nombreuses raisons, par exemple parce que l’utilisateur a activé ou désactivé une fonctionnalité, ou a déplacé l’application entre différents affichages ou que l’état d’alimentation du système a changé.

### <a name="universal-windows-platform-uwp-apps"></a>Applications plateforme Windows universelle (UWP)

Si vous écrivez une application UWP, quelle que soit l’API de rendu graphique que vous utilisez, utilisez [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) pour obtenir les fonctionnalités d’affichage. Obtenez une instance de **AdvancedColorInfo** à partir de [**DisplayInformation :: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Pour vérifier le type de couleurs avancé actuellement actif, utilisez la propriété [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) . Dans Windows 10, version 1903 et versions ultérieures, cette méthode retourne l’une des trois valeurs possibles : **SDR**, **WCG** ou **HDR**. Il s’agit de la propriété la plus importante à vérifier, et vous devez configurer votre pipeline de rendu et de présentation en réponse au genre actif.

Pour vérifier les types de couleurs avancés pris en charge, mais pas nécessairement actifs, appelez [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Vous pouvez utiliser ces informations, par exemple, pour inviter l’utilisateur à accéder à l’application Paramètres Windows afin qu’il puisse activer HDR ou WCG.

Les autres membres de **AdvancedColorInfo** fournissent des informations quantitatives sur le volume de couleurs physiques du panneau (luminance et chrominance), correspondant aux métadonnées HDR statiques 2086. Utilisez ces informations pour configurer le mappage HDR tonemapping et de gammes de votre application.

Pour gérer les modifications apportées aux fonctionnalités de couleur avancées, inscrivez-vous à l’événement [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) . Cet événement est déclenché si un paramètre des fonctionnalités de couleur avancées de l’affichage change pour une raison quelconque.

Gérez cet événement en obtenant une nouvelle instance de **AdvancedColorInfo** et en vérifiant les valeurs qui ont changé.

### <a name="desktop-win32-directx-apps"></a>Applications DirectX Desktop (Win32)

Si vous écrivez une application Win32 et utilisez DirectX pour effectuer le rendu, utilisez [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) pour obtenir des fonctionnalités d’affichage. Obtenez une instance de ce struct via [**IDXGIOutput6 :: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Pour vérifier le type de couleurs avancé actuellement actif, utilisez la propriété **ColorSpace** , qui est de type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), et contient l’une des valeurs suivantes :

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> D’autres types de couleurs avancés, tels que WCG, sont traités comme SDR par DXGI. Vous ne pouvez pas utiliser DXGI pour identifier un affichage WCG.

> [!Note]
> DXGI ne vous permet pas de vérifier les types de couleurs avancés qui sont pris en charge, mais qui ne sont pas actifs pour le moment.

La plupart des autres membres de **DXGI_OUTPUT_DESC1** fournissent des informations quantitatives sur le volume de couleurs physiques du panneau (luminance et chrominance), correspondant aux métadonnées HDR statiques 2086. Utilisez ces informations pour configurer le mappage HDR tonemapping et de gammes de votre application.

Les applications Win32 n’ont pas de mécanisme natif pour répondre aux modifications de capacité de couleurs avancées. Au lieu de cela, si votre application utilise une boucle de rendu, vous devez interroger [**IDXGIFactory1 :: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) avec chaque frame. Si elle indique **false**, vous devez obtenir un nouveau **DXGI_OUTPUT_DESC1** et vérifier les valeurs qui ont changé.

En outre, votre pompe de messages Win32 doit gérer le [**WM_SIZE**](../winmsg/wm-size.md) message, ce qui indique que votre application peut avoir été déplacée entre différents affichages.

> [!Note]
> Pour obtenir une nouvelle **DXGI_OUTPUT_DESC1**, vous devez obtenir l’affichage actuel. Toutefois, vous ne devez pas appeler **IDXGISwapChain :: GetContainingOutput**. Cela est dû au fait que les chaînes de permutation retournent une sortie DXGI obsolète une fois que **DXGIFactory :: IsCurrent** a la valeur false et que la recréation de la chaîne de permutation pour obtenir une sortie actuelle se traduit par un écran noir temporaire. Au lieu de cela, nous vous recommandons d’énumérer les limites de toutes les sorties DXGI et de déterminer celle qui a le plus d’intersection avec les limites de la fenêtre de votre application.

L’exemple de code suivant provient du [référentiel DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

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

## <a name="setting-up-your-directx-swap-chain"></a>Configuration de votre chaîne d’échange DirectX

Une fois que vous avez déterminé que l’affichage prend actuellement en charge les fonctionnalités de couleur avancées, configurez votre chaîne de permutation comme suit.

### <a name="use-a-flip-presentation-model-effect"></a>Utiliser un effet de rotation du modèle de présentation

Lors de la création de votre chaîne de permutation à l’aide de **CreateSwapChainFor [HWND | Composition | CoreWindow]** , vous devez utiliser le modèle de retournement dxgi en sélectionnant l’option **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ou **DXGI_SWAP_EFFECT_FLIP_DISCARD** , ce qui rend votre chaîne de permutation éligible pour le traitement des couleurs avancé à partir de DWM et diverses optimisations en plein écran. Pour plus d’informations, reportez-vous à la rubrique [pour obtenir des performances optimales, utiliser dxgi Flip Model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Option 1. Utiliser le format de pixel FP16 et l’espace de couleurs ScRVB

Windows 10 prend en charge deux combinaisons principales du format de pixel et de l’espace colorimétrique pour la couleur avancée. Sélectionnez-en un en fonction des exigences spécifiques de votre application.

Pour les applications à usage général, lors de la création de votre chaîne de permutation, nous vous recommandons de spécifier [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). C’est ce que l’on appelle également *FP16* dans votre [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Par défaut, une chaîne de permutation créée avec un format de pixel à virgule flottante est traitée comme si elle utilise l’espace de couleurs [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , également appelé *ScRVB*.

Cette combinaison vous fournit la plage numérique et la précision pour spécifier presque toutes les couleurs physiquement possibles et effectuer un traitement arbitraire, y compris une fusion. En outre, si vous utilisez Direct2D, Win2D ou Windows. UI. composition, il s’agit de la seule combinaison prise en charge pour toute chaîne de permutation ou cible intermédiaire qui contient du contenu de couleur avancé. 

Le principal inconvénient de cette option est qu’elle consomme 64 bits par pixel, ce qui double la bande passante du GPU et la consommation de mémoire par rapport aux formats de pixel de la base de SDR. En outre, ScRVB utilise des valeurs numériques qui se trouvent en dehors de la plage normalisée [0, 1] pour représenter les couleurs qui sont en dehors de la gamme sRVB et/ou supérieures à 80 nits de luminance. Par exemple, ScRVB (1,0, 1,0, 1,0) encode le blanc D65 standard à 80 nits ; Toutefois, ScRVB (12,5, 12,5, 12,5) encode le même blanc D65 à une plus grande luminosité de 1000 nits. Certaines opérations graphiques nécessitent une plage numérique normalisée et vous devez soit modifier l’opération, soit renormaliser les valeurs de couleur.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Option 2 : utiliser le format de pixel UINT10/RGB10 et l’espace de couleurs HDR10/BT. 2100

Pour les applications qui consomment du contenu encodé HDR10, tels que des lecteurs multimédias ou des applications qui doivent être utilisés principalement dans des scénarios en plein écran tels que des jeux, lors de la création de votre chaîne de permutation, vous devez envisager de spécifier [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) dans [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Par défaut, il est traité comme utilisant l’espace de couleurs sRVB. par conséquent, vous devez appeler explicitement [**IDXGISwapChain3 :: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)et définir comme espace de couleurs [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), également appelé HDR10/BT. 2100.

Cette combinaison présente des restrictions plus strictes que FP16. Vous pouvez l’utiliser uniquement avec Direct3D 11 ou Direct3D 12. En outre, UINT10/HDR10 présente des limitations sous la forme d’un format intermédiaire, car il utilise la fonction ST. 084 EOTF (fonction « gamma »), qui est très non linéaire et optimisée comme format câble, et parce qu’il n’offre que 2 bits d’alpha.

Toutefois, cette combinaison peut offrir des optimisations de performances puissantes lorsqu’elle est utilisée dans la sortie finale de votre application. Il consomme les mêmes 32 bits par pixel que les formats de pixel de l’SDR UINT8 traditionnels. En outre, dans certains scénarios en plein écran, le système d’exploitation peut optimiser les performances en analysant directement la surface HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Utilisation d’une chaîne d’échange de couleurs avancée lorsque l’affichage est en mode SDR

Vous pouvez utiliser une chaîne d’échange de couleurs avancée même si l’affichage ne prend pas en charge une partie ou la totalité des fonctionnalités de couleur avancées requises par votre contenu. Dans ce cas, le Gestionnaire de fenêtrage (DWM) downconvert votre contenu pour l’adapter aux fonctionnalités de l’affichage. Dans Windows 10, version 1903 et versions ultérieures, le découpage numérique sera effectué. par exemple, si vous affichez une chaîne de permutation FP16 ScRVB, tout en dehors de la plage numérique [0, 1] est tronqué.

Ce comportement downconversion se produira également si votre fenêtre d’application chevauche plusieurs affichages avec des fonctionnalités de couleur avancées différentes. **AdvancedColorInfo** et **IDXGIOutput6** sont abstraits pour signaler uniquement les caractéristiques de l’affichage « principal » (définies comme affichage contenant le centre de la fenêtre).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Restituer correctement le contenu SDR avec le niveau de référence SDR

Dans de nombreux scénarios, votre application souhaite afficher le contenu SDR et HDR. par exemple, le rendu des sous-titres ou des contrôles de transport sur une vidéo HDR ou une interface utilisateur dans une scène de jeu. Il est important de comprendre le concept de *niveau de référence SDR* pour vous assurer que votre contenu SDR semble correct sur un affichage HDR.

Windows traite le contenu HDR comme étant _référencé par scène_, ce qui signifie qu’une valeur de couleur particulière doit être affichée à un niveau de luminance spécifique. par exemple, ScRVB (1,0, 1,0, 1,0) et HDR10 (497, 497, 497) encodent exactement D65 en blanc à 80 nits de luminance. Pendant ce temps, le contenu SDR est traditionnellement soumis à la _sortie_ (ou à l’affichage), ce qui signifie que sa luminance est laissée à l’utilisateur ou à l’appareil ; par exemple, sRVB (1,0, 1,0, 1,0) encode le blanc D65 comme dans les exemples HDR, mais à toute luminance maximale pour laquelle l’affichage est configuré. Windows permet à l’utilisateur d’ajuster le _niveau de référence SDR_ à sa préférence. Il s’agit de la luminance que Windows restituera sRVB (1,0, 1,0, 1,0) à. Sur les moniteurs HDR de bureau, les niveaux de référence SDR sont généralement définis sur environ 200 nits.

> [!Note]
> Sur un écran qui prend en charge un contrôle de luminosité, par exemple sur un ordinateur portable, Windows ajuste également la luminance du contenu HDR (référencé par une scène) pour qu’il corresponde au niveau de luminosité souhaité de l’utilisateur, mais ce n’est pas visible pour l’application. À moins que vous n’essayiez de garantir une reproduction exacte du signal HDR, vous pouvez généralement l’ignorer.

Si votre application affiche toujours les SDR et HDR pour séparer les surfaces et s’appuie sur la composition du système d’exploitation, Windows effectue automatiquement l’ajustement correct pour augmenter le contenu SDR au niveau de blanc souhaité. Par exemple, si votre application utilise XAML et restitue le contenu HDR à son propre **SwapChainPanel**.

Toutefois, si votre application effectue sa propre composition de contenu SDR et HDR en une seule surface, vous êtes chargé d’effectuer vous-même le réglage du niveau de référence SDR. Sinon, le contenu SDR peut sembler trop sombre en supposant des conditions d’affichage de bureau typiques. Tout d’abord, vous devez obtenir le niveau de référence SDR actuel, puis vous devez ajuster les valeurs de couleur de tout contenu SDR que vous rendez.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Étape 1. Obtenir le niveau de référence SDR actuel

Actuellement, seules les applications UWP peuvent obtenir le niveau de référence SDR actuel via [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Cette API requiert un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Étape 2. Ajuster les valeurs de couleur du contenu SDR

Windows définit le niveau de référence nominal, ou par défaut, à 80 nits ; par conséquent, si vous deviez restituer un sRGB standard (1,0, 1,0, 1,0) blanc dans une chaîne de permutation FP16, il serait reproduit à une luminance de 80 nits. Afin de faire correspondre le niveau de référence défini par l’utilisateur réel, vous devez ajuster le contenu SDR de 80 Nits au niveau spécifié via **AdvancedColorInfo. SdrWhiteLevelInNits**.

Si vous effectuez un rendu à l’aide de FP16 et ScRVB, ou de tout espace colorimétrique qui utilise le gamma linéaire (1,0), vous pouvez simplement multiplier la valeur de couleur SDR par _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_. Si vous utilisez Direct2D, il existe une constante prédéfinie [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), qui a la valeur 80.

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

Si vous effectuez un rendu à l’aide d’un espace de couleurs gamma non linéaire tel que HDR10, le réglage du niveau de blanc SDR est plus complexe. Si vous écrivez votre propre nuanceur de pixels, vous devez envisager d’effectuer une conversion en gamma linéaire pour appliquer l’ajustement.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Adapter le contenu HDR aux fonctionnalités de l’affichage à l’aide de tonemapping

Les affichages couleur HDR et couleurs avancées varient considérablement en termes de fonctionnalités. Par exemple, la luminance minimale et maximale et la gamme de couleurs qu’elles peuvent reproduire. Dans de nombreux cas, votre contenu HDR contient des couleurs qui dépassent les capacités de l’affichage. Pour une qualité d’image optimale, il est important que vous effectuiez des tonemapping HDR, en compressant essentiellement la plage de couleurs pour l’adapter à l’affichage tout en préservant l’objectif visuel du contenu.

Le paramètre unique le plus important à adapter à la luminance est Max, également appelé MaxCLL (niveau de lumière du contenu); les tonemappers plus sophistiquées vont également adapter les fonctions de luminance minimale (MinCLL) et/ou les couleurs primaires.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Étape 1. Obtenir les capacités de volume de couleurs de l’affichage

#### <a name="universal-windows-platform-uwp-apps"></a>Applications plateforme Windows universelle (UWP)

Utilisez [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) pour obtenir le volume de couleurs de l’affichage.

#### <a name="win32-desktop-directx-apps"></a>Applications DirectX Win32 (Desktop)

Utilisez [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) pour obtenir le volume de couleurs de l’affichage.

### <a name="step-2-get-the-contents-color-volume-information"></a>Étape 2. Récupérer les informations sur les volumes de couleurs du contenu

Selon l’origine de votre contenu HDR, il existe plusieurs façons possibles de déterminer sa luminance et les informations de la gamme de couleurs. Certains fichiers vidéo et images HDR contiennent des métadonnées SMPTE ST. 2086. Si votre contenu a été rendu dynamiquement, vous pourrez peut-être extraire des informations de scène à partir des étapes de rendu internes, par exemple la source de lumière la plus brillante dans une scène.

Une solution plus générale mais gourmande en calculs consiste à exécuter un histogramme ou une autre analyse sur le cadre rendu. L' [exemple du kit de développement logiciel (SDK) des images de couleurs avancées de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) montre comment procéder à l’aide de Direct2D ; les extraits de code les plus pertinents sont inclus ci-dessous :

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

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Étape 3. Effectuer l’opération HDR tonemapping

Tonemapping est fondamentalement un processus de perte et peut être optimisé pour un certain nombre de mesures de perception ou objectives, donc il n’y a pas d’algorithme standard. Windows fournit un [effet Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) intégré dans le cadre de Direct2D et dans le pipeline de lecture vidéo HDR Media Foundation. Parmi les autres algorithmes couramment utilisés figurent les ACE cinématographiques, Reinhard et ITU-R BT. 2390-3 EETF (fonction de transfert électrique électrique).

Un opérateur Reinhard Tonemapper simplifié est illustré ci-dessous.

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

## <a name="capturing-hdr-and-wcg-content"></a>Capture de contenu HDR et WCG

Les API qui prennent en charge la spécification des formats de pixel, tels que ceux de l’espace de noms [**Windows. Graphics. capture**](/uwp/api/windows.graphics.capture) et de la méthode [**IDXGIOutput5 ::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , permettent de capturer le contenu HDR et WCG sans perdre les informations sur les pixels. Notez qu’après avoir acquis des trames de contenu, un traitement supplémentaire est nécessaire. Par exemple, le mappage de tonalité HDR-à-SDR (par exemple, capture de capture d’écran SDR pour le partage Internet) et l’enregistrement de contenu avec le format approprié (par exemple, JPEG XR).

## <a name="additional-resources"></a>Ressources supplémentaires

* *Utilisation du rendu HDR avec le kit d’outils DirectX* pour [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Procédure pas à pas d’ajout de la prise en charge HDR à une application DirectX à l’aide du kit d’outils DirectX (DirectXTK).
* [Exemple du kit de développement logiciel (SDK) couleurs avancées de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). Exemple SDK UWP mettant en œuvre une visionneuse d’images HDR et WCG avec prise en charge des couleurs avancées à l’aide de Direct2D. Illustre la gamme complète des meilleures pratiques pour les applications UWP, y compris la réponse aux modifications de capacité d’affichage et le réglage du niveau de blanc SDR.
* [Exemple de bureau HDR Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Exemple de SDK Desktop mettant en œuvre une scène HDR Direct3D 12 de base.
* [Exemple UWP Direct3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). Équivalent UWP de l’exemple ci-dessus.
* [Exemple de PC Xbox ATG SimpleHDR](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Exemple de SDK Desktop mettant en œuvre une scène HDR de base Direct3D 11.
