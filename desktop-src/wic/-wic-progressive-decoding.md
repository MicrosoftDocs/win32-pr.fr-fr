---
description: Cette rubrique présente le décodage progressif et l’utilisation du décodage progressif dans les applications.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Vue d’ensemble du décodage progressif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a409a337ecd3852a50cb5ca1a410ebd32c7f3226c79aacca20b10733e214fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710040"
---
# <a name="progressive-decoding-overview"></a>Vue d’ensemble du décodage progressif

Cette rubrique présente le décodage progressif et l’utilisation du décodage progressif dans les applications. Il fournit également des instructions pour la création de codecs qui prennent en charge le décodage progressif.

Cette rubrique contient les sections suivantes.

-   [Introduction](#introduction)
-   [Qu’est-ce que le décodage progressif ?](#what-is-progressive-decoding)
-   [prise en charge du décodage progressif dans Windows 7](#progressive-decoding-support-in-windows-7)
-   [Décodage progressif JPEG](#jpeg-progressive-decoding)
-   [Décodage progressif PNG/GIF](#pnggif-progressive-decoding)
    -   [Décodage progressif PNG](#png-progressive-decoding)
    -   [Décodage progressif GIF](#gif-progressive-decoding)
-   [Décodage progressif dans les applications](#progressive-decoding-in-applications)
-   [Prise en charge du codec personnalisé pour le décodage progressif](#custom-codec-support-for-progressive-decoding)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le décodage progressif permet de décoder et de restituer de façon incrémentielle des parties d’une image avant la fin du téléchargement de l’image entière. Cette fonctionnalité améliore considérablement l’expérience de l’utilisateur lors de l’affichage d’images à partir d’Internet, car l’utilisateur n’a pas besoin d’attendre que l’intégralité de l’image soit téléchargée avant de commencer le décodage. Les utilisateurs peuvent voir une image en préversion avec des données disponibles avant le téléchargement de l’image entière. Cette fonctionnalité est essentielle pour toute application utilisée pour afficher des images à partir d’Internet ou de sources de données avec une bande passante limitée.

le composant WIC (Windows Imaging Component) de Windows 7 prend en charge le décodage progressif des formats d’image populaires tels que JPEG, PNG et GIF. WIC prend également en charge tous les codecs non Microsoft compatibles WIC qui implémentent le décodage progressif. L’encodage progressif n’est pas pris en charge dans la version actuelle de WIC. cette rubrique décrit le décodage progressif dans Windows 7 et la procédure d’activation du décodage progressif dans vos applications.

## <a name="what-is-progressive-decoding"></a>Qu’est-ce que le décodage progressif ?

Le décodage progressif est la possibilité de décoder de façon incrémentielle des parties d’une image à partir d’un fichier image incomplet. Le décodage traditionnel nécessite un fichier image complet avant que le décodage puisse commencer. Le décodage progressif démarre à l’issue du téléchargement d’un niveau progressif d’une image. Le décodeur effectue une passe de décodage sur le niveau de progression progressive actuel de l’image. Il effectue ensuite plusieurs passes de décodage sur l’image lorsque chaque niveau progressif est téléchargé. Chaque passe de décodage révèle plus d’images jusqu’à ce que l’image soit entièrement téléchargée et décodée. Le nombre de passes requis pour décoder une image complète dépend du format du fichier image et du processus d’encodage utilisé pour créer l’image.

Les images doivent être codées spécifiquement pour implémenter le décodage progressif, mais tous les formats d’image ne la prennent pas en charge. La liste suivante résume les conditions requises pour l’utilisation du décodage progressif.

-   Le fichier image doit prendre en charge le décodage progressif. La plupart des formats d’image ne prennent pas en charge le décodage progressif, bien que les formats d’image classiques JPEG, PNG et GIF.
-   Le fichier image doit être encodé sous la forme d’une image progressive. Les fichiers image qui n’ont pas été créés avec l’encodage d’image progressive ne peuvent pas implémenter le décodage progressif, même si le format de fichier le prendrait autrement en charge.
-   Un codec qui prend en charge le décodage progressif doit être disponible. Si un codec ne prend pas en charge le décodage progressif, une image encodée en tant qu’image progressive est décodée comme une image traditionnelle.

## <a name="progressive-decoding-support-in-windows-7"></a>prise en charge du décodage progressif dans Windows 7

Windows 7 fournit des codecs intégrés qui prennent en charge le décodage progressif pour les formats d’image JPEG, PNG et GIF. chacun de ces codecs Windows 7 effectue plusieurs passes de décodage sur une image. Chaque passe correspond à un niveau particulier et à une partie de l’image qui est décodée, ce qui finit par aboutir à une image entièrement décodée.

Chaque format d’image gère le décodage progressif d’une manière différente. le tableau suivant fournit des informations sur le nombre de niveaux progressifs et la méthode de décodage prise en charge par les formats de décodage progressifs Windows 7. 

| Format d'image | Nombre de niveaux progressifs pris en charge | Méthode de décodage progressif |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Défini par l’image                       | Amélioration de la résolution       |
| PNG          | 7                                      | Entrelacement                 |
| GIF          | 4                                      | Entrelacement                 |



 

En outre, le décodage progressif peut être implémenté dans les codecs en fournissant une prise en charge des interfaces et des méthodes progressives. Si le décodage progressif n’est pas pris en charge dans un codec, les messages d’erreur appropriés doivent être retournés si ces méthodes sont appelées.

## <a name="jpeg-progressive-decoding"></a>Décodage progressif JPEG

Le décodage progressif JPEG présente des données d’image à des résolutions de plus en plus élevées pour chaque niveau, jusqu’à ce que l’image de haute résolution soit disponible. Chaque niveau de l’image est défini de façon à fournir un niveau de résolution différent. À mesure que des niveaux progressifs deviennent disponibles, l’image est affichée à des résolutions plus élevées, jusqu’à ce que l’image de résolution complète soit résolue.

Le nombre de niveaux disponibles et la résolution définie à chaque niveau dépendent entièrement du JPEG encodé. Les deux images suivantes montrent un exemple de décodage progressif JPEG à deux niveaux progressifs.

![exemples de décodage progressif JPEG](graphics/Progressive_JPEG_Comparison.jpg)

L’image à gauche est décodée au niveau progressif 0. L’image à droite est entièrement décodée après cinq niveaux progressifs.

## <a name="pnggif-progressive-decoding"></a>Décodage progressif PNG/GIF

Le décodage progressif PNG et GIF utilise une méthode de décodage progressive entrelacée. Le processus de décodage pour les deux formats est très similaire.

### <a name="png-progressive-decoding"></a>Décodage progressif PNG

Les fichiers image PNG proposent sept niveaux progressifs pour le décodage, comme décrit dans la spécification PNG. Le décodage progressif PNG est implémenté par le décodage d’un modèle spécifié de pixels à chaque passe du décodeur. Le modèle dans le tableau suivant de la spécification PNG est répliqué sur l’intégralité de l’image. Chaque nombre représente le niveau progressif dans lequel le pixel correspondant sera décodé.



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

Dans le tableau ci-dessus, vous pouvez déterminer les pixels qui seront décodés à chaque passe du décodeur. contrairement au codec GIF Windows 7, le codec PNG Windows 7 réplique le pixel le plus à gauche sur une ligne de numérisation pour remplir les pixels vides.

les images suivantes montrent un exemple du codec de décodage progressif PNG Windows 7 à trois niveaux progressifs.

![exemples de décodage progressif png](graphics/PNG_Progressive_Comparison.jpg)

L’image en haut à gauche montre une image PNG décodée au niveau progressif 0. L’image en haut à droite affiche la même image PNG décodée au niveau progressif 3. L’image inférieure affiche la même image entièrement décodée après 7 niveaux progressifs.

### <a name="gif-progressive-decoding"></a>Décodage progressif GIF

Les fichiers image GIF fournissent quatre niveaux progressifs pour le décodage, comme décrit dans la spécification GIF. Chaque passe remplit certaines lignes au sein d’une image, produisant une image complète après le quatrième passage. Le tableau suivant de la spécification GIF indique les lignes de numérisation qui sont décodées par chaque passe du décodeur. 

| Numéro de niveau/numéro de passe | Lignes de numérisation remplies   | Démarrage de la ligne de numérisation |
|---------------------------|------------------------|--------------------|
| 1                         | Chaque huitième ligne de numérisation | 0                  |
| 2                         | Chaque huitième ligne de numérisation | 4                  |
| 3                         | Chaque quatrième ligne d’analyse | 2                  |
| 4                         | Chaque seconde ligne d’analyse | 1                  |



 

bien que les codecs puissent spécifier le contenu de pixels vides à un niveau particulier, le codec GIF Windows remplit les lignes d’analyse vides en répliquant les lignes de numérisation remplies au-dessus de la ligne de numérisation vide.

## <a name="progressive-decoding-in-applications"></a>Décodage progressif dans les applications

L’interface de décodage progressive principale est l’interface [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) . Pour obtenir une référence à l’interface, interrogez une trame d’image ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) pour **IWICProgressiveLevelControl**. Les méthodes progressives sont ensuite accessibles à partir de l’interface.

Le code ci-dessous fournit un exemple d’utilisation du décodage progressif dans les applications.


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



Le code précédent fournit les fonctionnalités de base nécessaires pour implémenter le décodage progressif dans la plupart des applications. À l’aide du code, vous pouvez accéder aux niveaux progressifs, car les données de pixels de l’image deviennent disponibles. La fonction [**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) bloque l’exécution jusqu’à ce que le niveau demandé soit disponible.

## <a name="custom-codec-support-for-progressive-decoding"></a>Prise en charge du codec personnalisé pour le décodage progressif

Les développeurs de codec peuvent choisir d’implémenter le [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) si leurs formats d’image prennent en charge le décodage progressif. La prise en charge du décodage progressif n’est pas obligatoire pour la découverte et l’arbitrage par WIC. Toutefois, le décodage progressif améliore de manière importante l’expérience utilisateur et l’implémentation doit être prise en compte dans la mesure du possible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Compression et codage numériques de Continuous-Tone images fixes-exigences et recommandations](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[Format d’échange de fichier JPEG](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[Spécification GIF89a](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Spécification et extensions de Portable Network Graphics (PNG)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



