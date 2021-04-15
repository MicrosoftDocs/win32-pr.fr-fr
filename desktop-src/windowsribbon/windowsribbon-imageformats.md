---
title: Spécification des ressources d’image du ruban
description: En tant que système de présentation de commande riche, l’infrastructure de ruban Windows est conçue pour prendre en charge les ressources d’image de manière intensive tout au long de l’interface utilisateur du ruban. Toutes les ressources d’image sont déclarées dans le balisage du ruban ou interrogées à partir d’une application hôte du ruban.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Ruban Windows, ressources d’image
- Ruban, ressources d’image
- Ruban Windows, transparence
- Ruban, transparence
- Ruban Windows, profondeur de couleur
- Ruban, profondeur de couleur
- Ruban Windows, contraste
- Ruban, contraste
- ressources d’image dans le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463547"
---
# <a name="specifying-ribbon-image-resources"></a>Spécification des ressources d’image du ruban

En tant que système de présentation de commande riche, l’infrastructure de ruban Windows est conçue pour prendre en charge les ressources d’image de manière intensive tout au long de l’interface utilisateur du ruban. Toutes les ressources d’image sont déclarées dans le [balisage du ruban](windowsribbon-schema.md) ou interrogées à partir d’une application hôte du ruban.

Pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network Graphics) avec transparence.

Pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.

> [!Note]  
> Une erreur de compilation peut se produire si un format d’image non pris en charge est fourni à l’infrastructure.

 

## <a name="image-sizes"></a>Tailles d’image

Pour offrir une plus grande flexibilité pour les dispositions de contrôle de ruban lors du redimensionnement d’une fenêtre d’application, l’infrastructure du ruban accepte et affiche les images dans l’une des deux tailles suivantes : grande ou petite.

Les images suivantes illustrent une application de ruban qui prend en charge plusieurs tailles de ruban grâce à des dispositions de contrôle flexibles et au remplacement d’images volumineuses par des images de petite taille disponibles.

La capture d’écran suivante montre le ruban avec des images de grande taille pour les contrôles de zoom.

![capture d’écran montrant un ruban qui utilise des images de grande taille pour les contrôles de zoom.](images/overviews/imageresources-largeimage.png)

La capture d’écran suivante montre le même ruban redimensionné avec de petites images pour les contrôles de zoom

![capture d’écran montrant un ruban qui utilise de petites images pour les contrôles de zoom.](images/overviews/imageresources-smallimage.png)

La capture d’écran suivante montre le ruban dans un état masqué. Le ruban est masqué lorsque toutes les dispositions de contrôle potentielles ont été épuisées et que le ruban ne peut pas être rendu avec un espace de travail d’application utilisable.

![capture d’écran montrant un ruban réduit.](images/overviews/imageresources-noimage.png)

Pour toute image, la taille de pixel exacte dépend de la résolution d’affichage, ou des points par pouce (dpi), de l’analyse utilisée. À 96 ppp, les images volumineuses ont une taille de 32x32 pixels et les images de petite taille sont de 16 x 16 pixels. Les tailles d’image augmentent de manière linéaire par rapport à la fonction dpi, comme illustré dans le tableau suivant.



| PPP     | Petite image  | Grande image  |
|---------|--------------|--------------|
| 96 ppp  | 16x16 pixels | 32 x 32 pixels |
| 120 ppp | 20x20 pixels | 40 x 40 pixels |
| 144 PPP | 24x24 pixels | 48 pixels |
| 192 PPP | 32 x 32 pixels | 64x64 pixels |



 

L’infrastructure du ruban met à l’échelle les ressources d’image selon les besoins. Toutefois, étant donné que le redimensionnement peut générer des artefacts indésirables et une dégradation des images, il est fortement recommandé que l’application fournisse un petit ensemble de ressources d’image qui s’étendent sur différents paramètres ppp couramment utilisés. Si aucune correspondance exacte n’est trouvée, l’image la plus proche est mise à l’échelle vers le haut ou le bas.

Pour faciliter cette tâche, les ressources d’image peuvent être déclarées dans le balisage du ruban à l’aide d’un ensemble d’éléments [**image**](windowsribbon-element-image.md) pour chaque élément [**Command**](windowsribbon-element-command.md) . Au moment de l’exécution, l’infrastructure sélectionne l’image à afficher en fonction de l’attribut *MinDPI* de chaque élément **image** .

> [!IMPORTANT]
>
> Lorsqu’une collection de ressources d’image conçues pour prendre en charge des paramètres de résolution d’écran spécifiques est fournie à l’infrastructure du ruban via un ensemble d’éléments d' [**image**](windowsribbon-element-image.md) , l’infrastructure utilise l' **image** avec une valeur d’attribut *MinDPI* qui correspond au paramètre de dpi d’écran actuel.
>
> Si aucun élément [**image**](windowsribbon-element-image.md) n’est déclaré avec une valeur *MinDPI* qui correspond au paramètre PPP d’écran actuel, l’infrastructure sélectionne l' **image** qui a la valeur *MinDPI* la plus proche inférieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image. Sinon, si aucun élément **image** n’est déclaré avec une valeur d’attribut *MinDPI* inférieure au paramètre PPP d’écran actuel, le Framework choisit la valeur *MinDPI* la plus proche supérieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.

 

L’exemple suivant montre comment déclarer un ensemble d’images pour prendre en charge différentes tailles de ruban et paramètres système.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Si les images déclarées dans le balisage sont invalidées au moment de l’exécution pour une raison quelconque, l’application hôte est interrogée pour obtenir de nouvelles images. Lorsque ces images sont générées et chargées par programme, l’application doit tenter de retourner des images dimensionnées en fonction des tailles d’icône système par défaut déterminées par la [ \_ métrique du système CXICON SM](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Les images volumineuses ont une taille de SM \_ CXICON par SM \_ CXICON et les petites images ont une taille de SM \_ CXICON/2 par SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Profondeur des couleurs, transparence et contraste

Les images normales sont supposées être au format de pixel ARVB 32 bits par pixel (BPP) et être mises à l’échelle en fonction de la taille des icônes système par défaut. Ce format prend en charge la transparence et l’anticrénelage (à l’aide de 8 bits par canal).

> [!WARNING]
> De nombreux outils d’édition d’images ne conservent pas le canal alpha 8 bits d’ordre le plus élevé lors du chargement ou de l’enregistrement des images 32 BPP.

 

Pour qu’une image s’affiche correctement en mode de contraste élevé, elle doit être dans un format de pixel de palette de 4 BPP. Lorsque l’image est rendue, l’infrastructure du ruban remappe des couleurs spécifiques en fonction du contexte de contraste élevé de l’image.

Le tableau suivant répertorie le comportement de rendu des couleurs à contraste élevé de l’infrastructure.



Couleur du pixel

Valeur RVB

Comportement

Arrière-plan blanc

Arrière-plan foncé

MARRON

800080

Mode transparent

Mode transparent

FOND

000000

WINDOWTEXT de couleurs \_

AJOURÉE

AJOURÉE

FFFFFF

fenêtre de couleur \_

FOND

GRIS FONCÉ

808080

3DSHADOW de couleurs \_

3DSHADOW de couleurs \_

COCHÉ

C0C0C0

3DFACE de couleurs \_

3DFACE de couleurs \_

GRIS CLAIR

DFDFDF

3DLIGHT de couleurs \_

3DLIGHT de couleurs \_

BLEU FONCÉ

000080

n/a

AJOURÉE



 

Pour plus d’informations sur les formats d’image pris en charge par l’infrastructure du ruban, consultez les rubriques suivantes :

-   [Structure BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) -décrit le format de pixel 32 BPP ARVB.
-   [CreateDIBSection fonction](/windows/win32/api/wingdi/nf-wingdi-createdibsection) -décrit comment créer une image au format de pixel ARVB 32 BPP.
-   [LoadImage fonction](/windows/win32/api/winuser/nf-winuser-loadimagea) -décrit comment charger une image au format de pixel ARVB 32 BPP.

## <a name="accessibility"></a>Accessibilité

S’appuyer sur des ressources d’image pour fournir des informations, transmettre des fonctionnalités de contrôle et exposer l’état de l’application, augmente la nécessité d’exigences d’accessibilité lors de la conception et du développement de l’application.

Pour la prise en charge du contraste élevé de base, le ruban permet d’afficher un ensemble distinct de fichiers image quand un thème à contraste élevé est actif. Ces images peuvent être de 32 ou de 4 BPP, avec des couleurs mappées à une palette spéciale dans laquelle les couleurs sombres et claires sont inversées en fonction des couleurs de premier plan et d’arrière-plan du thème actif à contraste élevé.

L’exemple suivant montre comment les ressources d’image à contraste élevé sont déclarées dans le balisage du ruban :


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Commande. SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[IU \_ \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Commande. LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[IU \_ \_ LARGEIMAGE](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Commande. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[IU \_ \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Commande. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[IU \_ \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 