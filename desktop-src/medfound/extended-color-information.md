---
description: Informations sur les couleurs étendues
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Informations sur les couleurs étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ba43180a0f1e5253540088c1638f59d52380c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411198"
---
# <a name="extended-color-information"></a>Informations sur les couleurs étendues

Si vous avez des informations sur la couleur RVB, vous savez que (255, 255, 255) est l’triplet RVB 8 bits pour la couleur *blanche*. Mais quelle est la *couleur* réelle définie par cet triplet ?

La réponse peut être surprenant : sans informations supplémentaires, cet triplet ne définit pas de couleur particulière. La signification de toute valeur RVB dépend de l' *espace colorimétrique*. Si vous ne connaissez pas l’espace colorimétrique, vous ne connaissez pas la couleur.

Un espace colorimétrique définit la manière dont la représentation numérique d’une valeur de couleur donnée doit être reproduite comme lumière physique. Lorsque la vidéo est encodée dans un espace de couleurs, mais qu’elle est affichée dans une autre, les couleurs sont déformées, sauf si la vidéo est corrigée en couleurs. Pour obtenir une fidélité des couleurs précise, il est donc essentiel de connaître l’espace colorimétrique de la vidéo source. auparavant, le pipeline vidéo de Windows n’avait pas d’informations sur l’espace de couleurs prévu. à partir de Windows Vista, les DirectShow et les Media Foundation prennent en charge des informations de couleur étendues dans le type de média. Ces informations sont également disponibles pour DirectX Video Acceleration (DXVA).

La méthode standard pour décrire un espace colorimétrique mathématique consiste à utiliser l’espace de couleurs CIE XYZ, défini par la Commission internationale sur l’éclairage (CIE). Il n’est pas pratique d’utiliser les valeurs CIE XYZ directement dans la vidéo, mais l’espace de couleurs CIE XYZ peut être utilisé comme représentation intermédiaire lors de la conversion d’espaces de couleurs.

Pour reproduire les couleurs avec précision, les informations suivantes sont nécessaires :

-   Couleurs primaires. Les couleurs primaires définissent la façon dont les valeurs de tristimulus CIE XYZ sont représentées en tant que composants RVB. En effet, les couleurs primaires définissent la « signification » d’une valeur RVB donnée.
-   Fonction de transfert. La fonction de transfert est une fonction qui convertit les valeurs RGB linéaires en valeurs R’G’B non linéaires. Cette fonction est également appelée *correction gamma*.
-   Matrice de transfert. La matrice de transfert définit la façon dont R’G’B est converti en Y’PbPr.
-   Échantillonnage Chroma. La plupart des vidéos YUV sont transmises avec moins de résolution dans les composants de chrominance que la luminance. L’échantillonnage Chroma est indiqué par le FOURCC du format vidéo. Par exemple, YUY2 est un format 4:2:2, ce qui signifie que les échantillons de chrominance sont échantillonnés horizontalement par un facteur de 2.
-   Emplacement de chrominance. Lorsque la chrominance est échantillonnée, la position des échantillons de chrominance par rapport aux échantillons de luminance détermine la façon dont les échantillons manquants doivent être interpolés.
-   Plage nominale. La plage nominale définit le mode de mise à l’échelle des valeurs Y’PbPr vers Y’CbCr.

## <a name="color-space-in-media-types"></a>Espace colorimétrique dans les types de média

DirectShow, Media Foundation et DirectX Video Acceleration (DXVA) ont tous des moyens différents pour représenter les formats vidéo. Heureusement, il est facile de convertir les informations d’espace de couleurs d’une à l’autre, car les énumérations pertinentes sont les mêmes.

-   DXVA 1,0 : les informations sur l’espace colorimétrique sont fournies dans la structure [**DXVA \_ ExtendedFormat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) .
-   DXVA 2,0 : les informations sur l’espace colorimétrique sont fournies dans la structure de la structure [**DXVA2 \_ ExtendedFormat**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) . Cette structure est identique à la structure DXVA 1,0, et la signification des champs est la même.
-   DirectShow : les informations d’espace colorimétrique sont fournies dans la structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Les informations sont stockées dans les 24 bits supérieurs du champ **dwControlFlags** . Si des informations sur l’espace colorimétrique sont présentes, définissez l’indicateur **AMCONTROL \_ COLORINFO \_ present** dans **dwControlFlags**. Lorsque cet indicateur est défini, le champ **dwControlFlags** doit être interprété comme une [**structure \_ ExtendedFormat DXVA**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) , sauf que les 8 bits inférieurs de la structure sont réservés pour les indicateurs **AMCONTROL \_ xxx** .
-   Pilotes de capture vidéo : les informations sur l’espace colorimétrique sont fournies dans la structure [**\_ VIDEOINFOHEADER2 KS**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) . Cette structure est identique à la structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , et la signification des champs est la même.
-   Media Foundation : les informations d’espace colorimétrique sont stockées en tant qu’attributs dans le type de média :

    

    | Informations de couleur  | Attribut                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Couleurs primaires    | [**\_vidéos de \_ \_ réamorçage de la vidéo MF**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Fonction de transfert  | [**\_fonction de \_ transfert MF-MF \_**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matrice de transfert    | [**\_ \_ matrice YUV MT \_ YUV**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Sous-échantillonnage de chrominance | [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)<br/> (Fourni par le FOURCC, qui est stocké dans le premier **DWORD** du GUID de sous-type.)<br/> |
    | Emplacement de chrominance      | [**vidéo MF MT-présentation de \_ \_ \_ chrominance \_**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Plage nominale      | [**\_ \_ plage nominale de vidéo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversion de l’espace colorimétrique

La conversion d’un espace Y’CbCr à un autre requiert les étapes suivantes.

1.  Quantification inverse : convertissez la représentation Y’CbCr en représentation Y’PbPr, à l’aide de la plage nominale source.
2.  Échantillonnage : Convertissez les valeurs de chrominance échantillonnées en 4:4:4 en interpolant les valeurs de chrominance.
3.  Conversion YUV à RGB : convertir de Y’PbPr en R’G’B non linéaires, à l’aide de la matrice de transfert source.
4.  Fonction de transfert inverse : convertir un R’G’B non linéaire en RGB linéaire, à l’aide de l’inverse de la fonction de transfert.
5.  Conversion de l’espace colorimétrique RVB : utilisez les couleurs primaires pour passer de l’espace RVB source à l’espace RVB cible.
6.  Fonction de transfert : convertit le RGB linéaire en R’G’B non linéaire, à l’aide de la fonction de transfert cible.

7.  Conversion RGB en YUV : convertissez R’G’B’en Y’PbPr, à l’aide de la matrice de transfert cible.
8.  Sous-échantillonnage : convertissez 4:4:4 en 4:2:2, 4:2:0 ou 4:1:1 en filtrant les valeurs de chrominance.
9.  Quantification : convertissez Y’PbPr en Y’CbCr, à l’aide de la plage nominale cible.

Les étapes 1 à 4 se produisent dans l’espace de couleurs source et les étapes 6 à 9 se produisent dans l’espace de couleurs cible. Dans l’implémentation réelle, les étapes intermédiaires peuvent être approximatives et les étapes adjacentes peuvent être combinées. Il y a généralement un compromis entre la précision et le coût de calcul.

Par exemple, pour convertir de RT. 601 en RT. 709, vous devez effectuer les étapes suivantes :

-   Quantification inverse : Y’CbCr (601) à Y’PbPr (601)
-   Échantillonnage : Y’PbPr (601)
-   YUV à RVB : Y’PbPr (601) à R’G’B' (601)
-   Fonction de transfert inverse : R’G’B' (601) à RGB (601)
-   Conversion de l’espace colorimétrique RVB : RVB (601) en RVB (709)
-   Fonction de transfert : RVB (709) à R’G’B' (709)
-   RGB en YUV : R’G’B' (709) à Y’PbPr (709)
-   Sous-échantillonnage : Y’PbPr (709)

-   Quantification : Y’PbPr (709) à Y’CbCr (709)

## <a name="using-extended-color-information"></a>Utilisation des informations de couleurs étendues

Pour préserver la fidélité des couleurs dans l’ensemble du pipeline, les informations sur l’espace colorimétrique doivent être introduites au niveau de la source ou du décodeur et être transmises au récepteur via le pipeline.

### <a name="video-capture-devices"></a>Périphériques de capture vidéo

La plupart des périphériques de capture analogiques utilisent un espace de couleurs bien défini lors de la capture vidéo. Les pilotes de capture doivent offrir un format avec un bloc de format **KS \_ VIDEOINFOHEADER2** contenant les informations de couleur. Pour la compatibilité descendante, le pilote doit accepter des formats qui ne contiennent pas les informations de couleur. Cela permettra au pilote de fonctionner avec des composants qui n’acceptent pas les informations de couleur étendue.

### <a name="file-based-sources"></a>Sources basées sur des fichiers

lors de l’analyse d’un fichier vidéo, la source du média (ou le filtre de l’analyseur, dans DirectShow) peut être en mesure de fournir certaines informations de couleur. Par exemple, le navigateur DVD peut déterminer l’espace colorimétrique en fonction du contenu du DVD. D’autres informations de couleur peuvent être disponibles pour le décodeur. Par exemple, un flux vidéo élémentaire MPEG-2 fournit les informations de couleur dans le champ extension de l’affichage de la séquence \_ \_ . Si les informations de couleur ne sont pas explicitement décrites dans la source, elles peuvent être définies implicitement par le type de contenu. Par exemple, les variétés NTSC et PAL de vidéo DV utilisent chacune des espaces de couleurs différents. Enfin, le décodeur peut utiliser toutes les informations de couleur qu’il obtient du type de média de la source.

### <a name="other-components"></a>Autres composants

D’autres composants peuvent avoir besoin d’utiliser les informations d’espace colorimétrique dans un type de média :

-   Les convertisseurs d’espace colorimétrique logiciel doivent utiliser des informations d’espace colorimétrique lors de la sélection d’un algorithme de conversion.
-   Les mixages vidéo, tels que le mélangeur Video Enhancer (EVR), doivent utiliser les informations de couleur pour mélanger les flux vidéo de différents types de contenu.
-   Les API de traitement vidéo DXVA et DDIs permettent à l’appelant de spécifier des informations sur l’espace colorimétrique. Le GPU doit utiliser ces informations lorsqu’il effectue un mixage vidéo hardward.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
