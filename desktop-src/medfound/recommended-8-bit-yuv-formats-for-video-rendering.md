---
description: Formats YUV 8 bits recommandés pour le rendu vidéo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formats YUV 8 bits recommandés pour le rendu vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235896"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formats YUV 8 bits recommandés pour le rendu vidéo

Gary Sullivan et Stephen Estrop

Microsoft Corporation

2002 avril, mis à jour le 2008 novembre

cette rubrique décrit les formats de couleurs YUV 8 bits recommandés pour le rendu vidéo dans le système d’exploitation Windows. Cet article présente les techniques de conversion entre les formats YUV et RVB, et fournit également des techniques pour l’échantillonnage des formats YUV. Cet article est destiné aux personnes qui travaillent avec le décodage vidéo YUV ou le rendu dans Windows.

## <a name="introduction"></a>Introduction

De nombreux formats YUV sont définis dans l’ensemble du secteur de la vidéo. Cet article identifie les formats YUV 8 bits recommandés pour le rendu vidéo dans Windows. Les fournisseurs de décodeurs et les fournisseurs d’affichage sont encouragés à prendre en charge les formats décrits dans cet article. Cet article ne traite pas d’autres utilisations de la couleur YUV, telles que la photographie continue.

Les formats décrits dans cet article utilisent tous 8 bits par emplacement de pixel pour encoder le canal Y (également appelé canal de luminance) et utilisent 8 bits par échantillon pour encoder chaque échantillon de chrominance U ou V. Toutefois, la plupart des formats YUV utilisent moins de 24 bits par pixel en moyenne, car ils contiennent moins d’échantillons de vous et de V que de Y. Cet article ne couvre pas les formats YUV avec des canaux Y 10 bits ou plus.

> [!Note]  
> Dans le cadre de cet article, le terme U est équivalent à CB et le terme V équivaut à CR.

 

Cet article aborde les thèmes suivants :

-   [Échantillonnage YUV](#yuv-sampling). Décrit les techniques d’échantillonnage YUV les plus courantes.
-   [Définitions de surface](#surface-definitions). Décrit les formats YUV recommandés.
-   [Conversions de l’espace colorimétrique et du taux d’échantillonnage Chroma](#color-space-and-chroma-sampling-rate-conversions). Fournit des instructions pour la conversion entre des formats YUV et RGB et pour la conversion entre différents formats YUV.
-   [Identification des formats YUV dans Media Foundation](#identifying-yuv-formats-in-media-foundation). Explique comment décrire les types de format YUV dans Media Foundation.

## <a name="yuv-sampling"></a>Échantillonnage YUV

Les canaux Chroma peuvent avoir un taux d’échantillonnage inférieur à celui du canal de luminance, sans aucune perte spectaculaire de qualité de perception. Une notation appelée « A :B: C » est utilisée pour décrire la fréquence à laquelle vous et le V sont échantillonnés par rapport à Y :

-   4:4:4 signifie aucun sous-échantillonnage des canaux Chroma.
-   4:2:2 signifie un sous-échantillonnage horizontal de 2:1, sans sous-échantillonnage vertical. Chaque ligne de numérisation contient quatre échantillons Y pour chacun des deux échantillons U ou V.
-   4:2:0 signifie le sous-échantillonnage horizontal 2:1 de 2:1, avec un sous-échantillonnage vertical.
-   4:1:1 signifie un sous-échantillonnage horizontal de 4:1, sans sous-échantillonnage vertical. Chaque ligne de numérisation contient quatre échantillons Y pour chaque exemple V et V. 4:1:1 l’échantillonnage est moins courant que les autres formats, et n’est pas abordé en détail dans cet article.

Les diagrammes suivants montrent comment Chroma est échantillonné pour chaque fréquence de sous-échantillonnage. Les échantillons de luminance sont représentés par une croix, et les échantillons de chrominance sont représentés par un cercle.

![Figure 1. échantillonnage Chroma](images/yuv-sampling-grids.png)

La forme dominante de l’échantillonnage 4:2:2 est définie dans la recommandation ITU-R BT. 601. Il existe deux variantes courantes de l’échantillonnage 4:2:0. l’une d’elles est utilisée dans mpeg-2 video, tandis que l’autre est utilisée dans mpeg-1 et dans ITU-T Recommandations H. 261 et H. 263.

Comparé au schéma MPEG-1, il est plus simple de procéder à une conversion entre le schéma MPEG-2 et les grilles d’échantillonnage définies pour les formats 4:2:2 et 4:4:4. pour cette raison, le schéma MPEG-2 est préféré dans Windows et doit être considéré comme l’interprétation par défaut des formats 4:2:0.

## <a name="surface-definitions"></a>Définitions de surface

Cette section décrit les formats YUV 8 bits recommandés pour le rendu vidéo. Celles-ci appartiennent à plusieurs catégories :

-   [4:4:4 formats, 32 bits par pixel](#444-formats-32-bits-per-pixel)
-   [4:2:2 formats, 16 bits par pixel](#422-formats-16-bits-per-pixel)
-   [4:2:0 formats, 16 bits par pixel](#420-formats-16-bits-per-pixel)
-   [4:2:0 formats, 12 bits par pixel](#420-formats-12-bits-per-pixel)

Tout d’abord, vous devez connaître les concepts suivants pour comprendre ce qui suit :

-   *Origine* de la surface. Pour les formats YUV décrits dans cet article, l’origine (0,0) est toujours l’angle supérieur gauche de l’aire.
-   *Stride*. La largeur d’une surface, parfois appelée « tangage », est la largeur de la surface en octets. À partir de l’origine d’une surface dans le coin supérieur gauche, le Stride est toujours positif.
-   *Alignement*. L’alignement d’une surface est à la discrétion du pilote d’affichage graphique. La surface doit toujours être alignée sur la valeur DWORD. autrement dit, il est garanti que les lignes individuelles de la surface proviennent d’une limite de 32 bits (DWORD). Toutefois, l’alignement peut être supérieur à 32 bits, en fonction des besoins du matériel.
-   Format condensé et format Planar. Les formats YUV sont divisés en formats *compactés* et en formats *planaires* . Dans un format compressé, les composants Y, U et V sont stockés dans un tableau unique. Les pixels sont organisés en groupes de macropixels, dont la disposition dépend du format. Dans un format Planar, les composants Y, U et V sont stockés sous la forme de trois plans distincts.

Chaque format YUV décrit dans cet article est associé à un code FOURCC. Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.

-   4:4:4 (32 BPP)
    -   [AYUV](#ayuv)
-   4:2:2 (16 bpp)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 bpp)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 BPP)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>4:4:4 formats, 32 bits par pixel

### <a name="ayuv"></a>AYUV

Un format 4:4:4 unique est recommandé, avec le code FOURCC AYUV. Il s’agit d’un format compressé, où chaque pixel est encodé sous la forme de quatre octets consécutifs, organisés dans l’ordre indiqué dans l’illustration suivante.

![Figure 2. disposition de la mémoire ayuv](images/yuvformats01.gif)

Les octets marqués un contiennent des valeurs pour alpha.

## <a name="422-formats-16-bits-per-pixel"></a>4:2:2 formats, 16 bits par pixel

Deux formats 4:2:2 sont recommandés, avec les Codes FOURCC suivants :

-   YUY2
-   UYVY

Les deux sont des formats compactés, où chaque macropixel est codé sur deux pixels, sous la forme de quatre octets consécutifs. Cela entraîne un sous-échantillonnage horizontal du Chroma par un facteur de deux.

### <a name="yuy2"></a>YUY2

Dans le format YUY2, les données peuvent être traitées sous la forme d’un tableau de valeurs **char** non signées, où le premier octet contient le premier échantillon y, le deuxième octet contient le premier exemple U (CB), le troisième octet le deuxième y, et le quatrième octet le premier exemple V (CR), comme indiqué dans le diagramme suivant.

![Figure 3. disposition de la mémoire YUY2](images/yuvformats02.gif)

Si l’image est traitée comme un tableau de valeurs de **mot** Little-endian, le premier **mot** contient le premier échantillon Y dans les bits les moins significatifs (LSBs) et le premier exemple U (CB) dans les bits les plus significatifs (MSBS). Le deuxième **mot** contient le deuxième échantillon Y dans le LSBs et le premier exemple V (CR) dans le MSBS.

YUY2 est le format de pixel par défaut de 4:2:2 pour Microsoft DirectX Video Acceleration (DirectX VA). Il doit s’agir d’une exigence de terme intermédiaire pour les accélérateurs DirectX VA prenant en charge 4:2:2 vidéo.

### <a name="uyvy"></a>UYVY

Ce format est le même que le format YUY2, sauf que l’ordre d’octet est inversé, c’est-à-dire que les octets chrominance et luminance sont retournés (figure 4). Si l’image est traitée comme un tableau de deux valeurs de **mot** Little-endian, le premier **mot** contient U dans LSBs et Y0 dans le MSBS, et le deuxième **mot** contient V dans LSBs et Y1 dans le MSBS.

![Figure 4. disposition de la mémoire UYVY](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>4:2:0 formats, 16 bits par pixel

Deux formats de 4:2:0 16 bits par pixel (BPP) sont recommandés, avec les Codes FOURCC suivants :

-   IMC1
-   IMC3

Ces deux formats YUV sont des formats planaires. Les canaux Chroma sont sous-échantillonnés par un facteur de deux dans les dimensions horizontales et verticales.

### <a name="imc1"></a>IMC1

Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées. Cela est suivi de tous les exemples V (CR), puis de tous les exemples U (CB). Les plans V et U ont le même Stride que le plan Y, ce qui génère des zones de mémoire inutilisées, comme illustré à la figure 5. Les plans vous et V doivent commencer sur les limites de la mémoire qui sont un multiple de 16 lignes. La figure 5 illustre l’origine de vous et V pour une image vidéo 352 x 240. L’adresse de départ des plans vous et V est calculée comme suit :

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

où *py* est un pointeur d’octet vers le début du tableau de mémoire, comme indiqué dans le diagramme suivant.

![Figure 5. disposition de la mémoire imc1 (exemple)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Ce format est identique à IMC1, sauf que les plans vous et V sont permutés, comme indiqué dans le diagramme suivant.

![Figure 6. disposition de la mémoire imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 formats, 12 bits par pixel

Quatre formats 4:2:0 12-BPP sont recommandés, avec les Codes FOURCC suivants :

-   IMC2
-   IMC4
-   YV12
-   NV12

Dans tous ces formats, les canaux Chroma sont sous-échantillonnés par un facteur de deux dans les dimensions horizontales et verticales.

### <a name="imc2"></a>IMC2

Ce format est le même que IMC1, à l’exception de la différence suivante : les lignes V (CR) et U (CB) sont entrelacées à des limites de demi-Stride. En d’autres termes, chaque ligne complète de la zone Chroma commence par une ligne d’échantillons de V, suivie d’une ligne d’échantillons de U qui commence à la limite demi-Stride suivante (figure 7). Cette disposition permet une utilisation plus efficace de l’espace d’adressage que IMC1. Il coupe l’espace d’adressage chroma en moitié et, par conséquent, l’espace d’adressage total de 25%. Parmi les formats 4:2:0, IMC2 est le second format préféré, après NV12. L’illustration suivante montre ce processus.

![Figure 7. disposition de la mémoire imc2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Ce format est identique à IMC2, sauf que les lignes U (CB) et V (CR) sont échangées, comme le montre l’illustration suivante.

![Figure 8. disposition de la mémoire imc4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées. Ce tableau est immédiatement suivi par tous les exemples V (CR). Le Stride du plan V est la moitié du plan Y. et le plan V contient deux fois plus de lignes que le plan Y. Le plan V est immédiatement suivi par tous les exemples U (CB), avec les mêmes Stride et nombre de lignes que le plan V, comme indiqué dans l’illustration suivante.

![Figure 9. disposition de la mémoire YV12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Tous les échantillons Y apparaissent en premier dans la mémoire sous la forme d’un tableau de valeurs **char** non signées avec un nombre pair de lignes. Le plan Y est immédiatement suivi d’un tableau de valeurs **char** non signées qui contient des exemples empaquetés U (CB) et V (CR). Quand le tableau U-V combiné est adressé sous la forme d’un tableau de valeurs de **mot** Little-endian, LSBs contient les valeurs U et MSBS contient les valeurs V. NV12 est le format de pixel par défaut de 4:2:0 pour DirectX VA. Il doit s’agir d’une exigence de terme intermédiaire pour les accélérateurs DirectX VA prenant en charge 4:2:0 vidéo. L’illustration suivante montre le plan Y et le tableau contenant les exemples empaquetés et V.

![Figure 10. disposition de la mémoire nv12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversions de l’espace colorimétrique et du taux d’échantillonnage Chroma

Cette section fournit des instructions pour la conversion entre YUV et RVB, et pour la conversion entre différents formats YUV. Nous considérons deux schémas d’encodage RVB dans cette section : RVB d' *ordinateur 8 bits*, également connu sous le nom de RVB ou « RGB à l’échelle complète », et *vidéo de Studio Video RGB*, ou « RVB avec la salle de tête et la salle de remontée ». Ceux-ci sont définis comme suit :

-   L’ordinateur RGB utilise 8 bits pour chaque échantillon de rouge, vert et bleu. Le noir est représenté par R = G = B = 0 et le blanc est représenté par R = G = B = 255.
-   Studio Video RGB utilise un nombre de bits N pour chaque échantillon de rouge, vert et bleu, où N est supérieur ou supérieur à 8. Studio Video RGB utilise un facteur d’échelle différent de celui de l’ordinateur RGB et un décalage. Le noir est représenté par R = G = B = 16 \* 2 ^ (N-8) et le blanc est représenté par R = G = B = 235 \* 2 ^ (n-8). Toutefois, les valeurs réelles peuvent ne pas être comprises dans cette plage.

Studio video rgb est la définition rvb préférée pour la vidéo dans Windows, tandis que l’ordinateur rgb est la définition rvb préférée pour les applications non vidéo. Quelle que soit la forme RVB, les coordonnées chromatiques sont spécifiées dans ITU-R BT. 709 pour la définition des couleurs primaires RVB. Les coordonnées (x, y) de R, G et B sont (0,64, 0,33), (0,30, 0,60) et (0,15, 0,06), respectivement. Le blanc de référence est D65 avec les coordonnées (0,3127, 0,3290). La gamma nominal est de 1/0.45 (environ 2,2), avec un gamma précis défini en détail dans ITU-R BT. 709.

**Conversion entre RGB et 4:4:4 YUV**

Nous commençons par décrire la conversion entre RVB et 4:4:4 YUV. Pour convertir 4:2:0 ou 4:2:2 YUV en RGB, nous vous recommandons de convertir les données YUV en 4:4:4 YUV, puis de convertir de 4:4:4 YUV en RVB. Le format AYUV, qui est un format 4:4:4, utilise 8 bits chacun pour les exemples Y, U et V. Les YUV peuvent également être définis à l’aide de plus de 8 bits par échantillon pour certaines applications.

Deux conversions YUV dominantes de RGB ont été définies pour la vidéo numérique. Les deux reposent sur la spécification connue sous le nom de recommandation ITU-R BT. 709. La première conversion est l’ancienne forme YUV définie pour une utilisation de 50 Hz dans BT. 709. Il est identique à la relation spécifiée dans la recommandation ITU-R BT. 601, également connue par son ancien nom, CCIR 601. Il doit être considéré comme le format YUV préféré pour la résolution TV de définition standard (720 x 576) et la vidéo de faible résolution. Il est caractérisé par les valeurs de deux constantes *KR* et *KB*:

``` syntax
Kr = 0.299
Kb = 0.114
```

La deuxième conversion est le formulaire YUV plus récent défini pour une utilisation de 60 Hz dans BT. 709 et doit être considéré comme le format préféré pour les résolutions vidéo au-dessus de SDTV. Elle est caractérisée par différentes valeurs pour ces deux constantes :

``` syntax
Kr = 0.2126
Kb = 0.0722
```

La conversion de RVB en YUV est définie à partir de ce qui suit :

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

Les valeurs YUV sont ensuite obtenues comme suit :

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

where

-   M est le nombre de bits par échantillon YUV (M >= 8).
-   Z est la variable de niveau noir. Pour l’ordinateur RGB, Z est égal à 0. Pour Studio Video RGB, Z est égal à 16 \* 2 ^ (n-8), où N est le nombre de bits par échantillon RVB (n >= 8).
-   S est la variable de mise à l’échelle. Pour l’ordinateur RGB, S est égal à 255. Pour Studio Video Video RGB, S est égal à 219 \* 2 ^ (N-8).

La fonction Floor (x) retourne le plus grand entier inférieur ou égal à x. La fonction Clip3 (x, y, z) est définie comme suit :

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> Clip3 doit être implémenté en tant que fonction plutôt qu’en tant que macro de préprocesseur ; dans le cas contraire, plusieurs évaluations des arguments se produisent.

 

L’échantillon Y représente la luminosité et les exemples vous et V représentent les écarts de couleur par rapport au bleu et au rouge, respectivement. La plage nominale pour Y est 16 \* 2 ^ (m-8) à 235 \* 2 ^ (m-8). Le noir est représenté sous la forme 16 \* 2 ^ (m-8) et le blanc est représenté sous la forme 235 \* 2 ^ (m-8). La plage nominale pour vous et V est comprise entre 16 \* 2 ^ (m-8) et 240 \* 2 ^ (m-8), avec la valeur 128 \* 2 ^ (m-8) représentant le Chroma neutre. Toutefois, les valeurs réelles peuvent être en dehors de ces plages.

Pour les données d’entrée sous la forme Studio Video RGB, l’opération clip est nécessaire pour conserver les valeurs vous et V dans la plage 0 à (2 ^ M)-1. Si l’entrée est Computer RGB, l’opération de découpage n’est pas nécessaire, car la formule de conversion ne peut pas produire de valeurs en dehors de cette plage.

Il s’agit des formules exactes sans approximation. Tout ce qui suit dans ce document est dérivé de ces formules. Cette section décrit les conversions suivantes :

-   [Conversion de RGB888 en YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Conversion de YUV de 8 bits en RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Conversion de 4:2:0 YUV en 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Conversion de 4:2:2 YUV en 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Conversion de 4:2:0 YUV en 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Conversion de RGB888 en YUV 4:4:4

Dans le cas d’une entrée d’ordinateur RVB et de la sortie BT. 601 à 8 bits, nous pensons que les formules fournies dans la section précédente peuvent être raisonnablement approximatives par les éléments suivants :

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Ces formules produisent des résultats 8 bits utilisant des coefficients qui ne nécessitent pas plus de 8 bits de précision (non signée). Les résultats intermédiaires requièrent jusqu’à 16 bits de précision.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Conversion de YUV de 8 bits en RGB888

À partir des formules RVB-à-YUV d’origine, il est possible de dériver les relations suivantes pour BT. 601.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Par conséquent, étant donné :

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

les formules permettant de convertir YUV en RGB peuvent être dérivées comme suit :

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

où `clip()` dénote le découpage dans une plage de \[ 0.. 255 \] . Nous pensons que ces formules peuvent être raisonnablement approximatives par les éléments suivants :

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Ces formules utilisent des coefficients qui requièrent plus de 8 bits de précision pour produire chaque résultat de 8 bits, et les résultats intermédiaires nécessitent plus de 16 bits de précision.

Pour convertir 4:2:0 ou 4:2:2 YUV en RGB, nous vous recommandons de convertir les données YUV en 4:4:4 YUV, puis de convertir de 4:4:4 YUV en RVB. Les sections qui suivent présentent certaines méthodes pour convertir les formats 4:2:0 et 4:2:2 à 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Conversion de 4:2:0 YUV en 4:2:2 YUV

La conversion de 4:2:0 YUV en 4:2:2 YUV requiert une conversion verticale par un facteur de deux. Cette section décrit un exemple de méthode pour effectuer la conversion. La méthode suppose que les images vidéo sont une analyse progressive.

> [!Note]  
> Le processus de conversion d’analyse entrelacée de 4:2:0 à 4:2:2 présente des problèmes atypiques et est difficile à implémenter. Cet article ne traite pas du problème de conversion de l’analyse entrelacée de 4:2:0 à 4:2:2.

 

Laissez chaque ligne verticale d’échantillons de chrominance d’entrée être un tableau qui est compris `Cin[]` entre 0 et N-1. La ligne verticale correspondante sur l’image de sortie est un tableau `Cout[]` qui est compris entre 0 et 2n-1. Pour convertir chaque ligne verticale, procédez comme suit :

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

où clip () désigne le découpage dans une plage de \[ 0.. 255 \] .

> [!Note]  
> Les équations permettant de gérer les bords peuvent être simplifiées de façon mathématique. Ils sont présentés dans ce formulaire pour illustrer l’effet de verrouillage aux bords de l’image.

 

En effet, cette méthode calcule chaque valeur manquante en interpolant la courbe sur les quatre pixels adjacents, pondérée vers les valeurs des deux pixels les plus proches (figure 11). La méthode d’interpolation spécifique utilisée dans cet exemple génère des échantillons manquants à des positions semi-entières à l’aide d’une méthode connue appelée Catmull-Rom interpolation, également appelée interpolation de convolution cubique.

![Figure 11. Diagramme montrant l’échantillonnage 4:2:0 à 4:2:2](images/yuvformats14.gif)

Dans les termes du traitement des signaux, la conversion verticale doit idéalement inclure une compensation de décalage de phase pour tenir compte du décalage vertical de demi-pixel (par rapport à la grille d’échantillonnage 4:2:2 de sortie) entre les emplacements des exemples de lignes 4:2:0 et l’emplacement de chaque autre ligne d’exemple 4:2:2. Toutefois, l’introduction de ce décalage augmenterait la quantité de traitement nécessaire pour générer les exemples, et rendra impossible la reconstruction des exemples 4:2:0 originaux à partir de l’image 4:2:2. Il serait également impossible de décoder la vidéo directement en surfaces 4:2:2, puis d’utiliser ces surfaces comme images de référence pour décoder les images suivantes dans le flux. Par conséquent, la méthode fournie ici ne prend pas en compte l’alignement vertical précis des exemples. Cela n’est probablement pas nuisible visuellement à des résolutions d’image relativement élevées.

Si vous commencez avec la vidéo 4:2:0 qui utilise la grille d’échantillonnage définie dans H. 261, H. 263 ou MPEG-1 Video, la phase de l’échantillon de couleur 4:2:2 de sortie est également décalée d’un décalage horizontal 4:2:2 de demi-pixel par rapport à l’espacement sur la grille d’échantillonnage de luminance Toutefois, la forme MPEG-2 de 4:2:0 vidéo est probablement plus couramment utilisée sur les PC et ne subit pas de problème. En outre, la distinction n’est probablement pas dangereuse visuellement à des résolutions d’image relativement élevées. Si vous tentez de corriger ce problème, vous créerez le même type de problème que celui traité pour le décalage vertical de la phase.

## <a name="converting-422-yuv-to-444-yuv"></a>Conversion de 4:2:2 YUV en 4:4:4 YUV

La conversion de 4:2:2 YUV en 4:4:4 YUV requiert une conversion horizontale d’un facteur de deux. La méthode décrite précédemment pour la conversion verticale peut également être appliquée à la conversion horizontale. Pour les vidéos MPEG-2 et ITU-R BT. 601, cette méthode produira des exemples avec l’alignement de phase approprié.

## <a name="converting-420-yuv-to-444-yuv"></a>Conversion de 4:2:0 YUV en 4:4:4 YUV

Pour convertir 4:2:0 YUV en 4:4:4 YUV, vous pouvez simplement suivre les deux méthodes décrites précédemment. Convertissez l’image 4:2:0 en 4:2:2, puis convertissez l’image 4:2:2 en 4:4:4. Vous pouvez également basculer l’ordre des deux processus de conversion, car l’ordre des opérations n’a pas vraiment d’importance sur la qualité visuelle du résultat.

## <a name="other-yuv-formats"></a>Autres formats YUV

D’autres formats YUV les moins courants sont les suivants :

-   AI44 est un format en palette YUV avec 8 bits par échantillon. Chaque échantillon contient un index dans les 4 bits les plus significatifs (MSBs) et une valeur alpha dans les 4 bits les plus significatifs (LSBs). L’index fait référence à un tableau d’entrées de palette YUV, qui doit être défini dans le type de média pour le format. Ce format est principalement utilisé pour les images de sous-image.
-   NV11 est un format Planar 4:1:1 avec 12 bits par pixel. Les échantillons Y apparaissent en premier dans la mémoire. Le plan Y est suivi d’un tableau d’échantillons compactés U (CB) et V (CR). Quand le tableau U-V combiné est adressé sous la forme d’un tableau de valeurs de **mot** Little-endian, les échantillons u sont contenus dans le LSBs de chaque **mot**, et les exemples V sont contenus dans le MSBS. (Cette disposition de mémoire est similaire à NV12, bien que l’échantillonnage Chroma soit différent.)
-   Y41P est un format compressé de 4:1:1, avec vous et V échantillonnés tous les quatre pixels horizontalement. Chaque macropixel contient 8 pixels en trois octets, avec la disposition d’octets suivante : `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T est identique à Y41P, sauf que le bit le moins significatif de chaque échantillon Y spécifie la clé de chrominance (0 = transparent, 1 = opaque).
-   Y42T est identique à UYVY, sauf que le bit le moins significatif de chaque échantillon Y spécifie la clé de chrominance (0 = transparent, 1 = opaque).
-   YVYU est équivalent à YUYV, sauf que les exemples vous et V sont permutés.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identification des formats YUV dans Media Foundation

Chaque format YUV décrit dans cet article est associé à un code FOURCC. Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.

Il existe plusieurs macros C/C++ qui facilitent la déclaration de valeurs FOURCC dans le code source. Par exemple, la macro **MAKEFOURCC** est déclarée dans Mmsystem. h, et la macro **FCC** est déclarée dans Aviriff. h. Utilisez-les comme suit :

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères. Par exemple :

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

l’inversion de l’ordre est nécessaire, car le système d’exploitation Windows utilise une architecture little endian. 'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.

Dans Media Foundation, les formats sont identifiés par un GUID de type principal et un GUID de sous-type. Le type majeur pour les formats vidéo d’ordinateur est toujours MFMediaType \_ . Le sous-type peut être construit en mappant le code FOURCC à un GUID, comme suit :

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

où `XXXXXXXX` est le code FourCC. Par conséquent, le GUID de sous-type pour YUY2 est :

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Les constantes pour les GUID de format YUV les plus courants sont définies dans le fichier d’en-tête mfapi. h. Pour obtenir la liste de ces constantes, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la vidéo YUV](about-yuv-video.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 



