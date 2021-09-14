---
description: Entrelacement de vidéos
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelacement de vidéos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313606"
---
# <a name="video-interlacing"></a>Entrelacement de vidéos

Cette rubrique décrit comment les sources et les décodeurs multimédias doivent gérer le contenu vidéo entrelacé.

Pour décoder et restituer correctement la vidéo entrelacée, les informations suivantes sont nécessaires :

-   Progressif ou entrelacé. Un flux vidéo peut contenir des images progressives, des images entrelacées ou une combinaison des deux.

-   Dominante de champ. Zone dominante de champ décrit le champ qui apparaît en premier, le champ supérieur ou le champ inférieur.

-   Répéter le premier champ. Cet indicateur est utilisé dans la conversion 3:2, lorsque le frame est progressif mais que le flux est entrelacé. Dans ce contexte, le premier champ peut être le champ supérieur ou inférieur.

-   Champs entrelacés ou champ unique. Un exemple peut contenir un champ unique ou deux champs entrelacés. Si un échantillon contient un seul champ, la hauteur de l’échantillon correspond à la moitié de la hauteur du cadre, car l’échantillon contient uniquement la moitié des lignes de numérisation d’un cadre. Les champs entrelacés sont recommandés, à moins que les caractéristiques du contenu source ne stipulent dans le cas contraire.

L’une de ces caractéristiques peut passer d’un exemple à l’autre. Toutefois, les composants vidéo doivent connaître le contenu global avant le début de la diffusion. Par exemple, si la vidéo est entrelacée, le convertisseur vidéo amélioré (EVR) doit réserver de la mémoire vidéo pour la désentrelacement. En revanche, si la vidéo est entièrement progressive, les EVR peuvent optimiser le pipeline de rendu. L’ajout d’une étape de désentrelacement au pipeline augmente la latence de rendu.

Les informations relatives à l’entrelacement sont stockées à deux emplacements :

-   Les informations générales sur l’entrelacement dans un flux sont placées dans le type de média. Pour plus d’informations sur les types de médias, consultez [types de médias](media-types.md).

-   Les informations qui peuvent changer avec chaque exemple sont placées sur l’exemple en tant qu’attribut. Pour plus d’informations sur les exemples, consultez [Media Samples](media-samples.md)(en anglais).

## <a name="interlace-information-in-the-media-type"></a>Entrelacer les informations dans le type de média

L' [**attribut \_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md) sur le type de média décrit comment le flux dans son ensemble est entrelacé. La valeur de cet attribut est un membre de l’énumération [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) . Un type de média vidéo doit toujours avoir cet attribut.

-   Si le flux contient uniquement des images progressives, sans Frame entrelacé, utilisez MFVideoInterlace \_ progressive.
-   Si le flux contient uniquement des frames entrelacés et que chaque échantillon contient deux champs entrelacés, utilisez MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.
-   Si le flux contient uniquement des frames entrelacés et que chaque exemple contient un champ unique, utilisez MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower. Si les champs alternent entre le haut et le bas, il n’est pas important d’utiliser ces deux valeurs. Si le format contient uniquement des champs supérieurs, ou juste des champs inférieurs, définissez la valeur qui correspond au contenu.
-   Si le flux de contenu contient une combinaison de trames entrelacées et progressives, ou si le champ est défini sur le type de média, définissez le type de support sur MFVideoInterlace \_ MixedInterlaceOrProgressive. Utilisez des attributs d’exemple pour décrire chaque frame.

Le tableau suivant résume cet attribut.



| \_ \_ mode entrelacé MF-MT \_                       | Entrelacées? | Exemples                                  | Premier champ    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ progressif                 | Non          | Frame progressif                        | Non applicable |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | Oui         | Champs entrelacés                       | Haut en premier    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | Oui         | Champs entrelacés                       | En premier    |
| MFVideoInterlace \_ FieldSingleUpper            | Oui         | Champ unique                             | Haut en premier    |
| MFVideoInterlace \_ FieldSingleLower            | Oui         | Champ unique                             | En premier    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | Peut varier    | Champs entrelacés ou images progressives | Peut varier       |



 

Les champs entrelacés et les champs uniques ne peuvent pas être mélangés. Passer d’un à un autre nécessite une modification de type de média.

## <a name="interlace-flags-on-samples"></a>Entrelacer les indicateurs sur les échantillons

Les informations qui peuvent changer d’un exemple à l’autre sont indiquées à l’aide d’exemples d’attributs. Utilisez l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour récupérer ou définir ces attributs.

Tous les attributs d’entrelacement listés dans cette section ont des valeurs booléennes. En effet, chacun de ces attributs peut avoir trois valeurs : **true**, **false** ou not set. Si un attribut n’est pas défini, la valeur est extraite du type de média. Si un attribut est défini, la valeur remplace le type de média. Certaines combinaisons d’indicateurs et de types de média ne sont pas valides.




| Attribut | Description | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | Si la <strong>valeur est true</strong>, le frame est entrelacé. Si la <strong>valeur est false</strong>, le frame est progressif.<br /> Définissez cet attribut sur chaque exemple si le type de média est MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | La signification de cet indicateur varie selon que les exemples contiennent des champs entrelacés ou des champs uniques.<br /><ul><li>Champs entrelacés : si la <strong>valeur est true</strong>, le champ inférieur est tout d’abord. Si la <strong>valeur est false</strong>, le champ supérieur est tout d’abord.<br /></li><li>Champs uniques : si la <strong>valeur est true</strong>, l’exemple contient un champ inférieur. Si la <strong>valeur est false</strong>, l’exemple contient un champ supérieur.<br /></li></ul>Définissez cet attribut sur chaque échantillon entrelacé si le type de média est MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower ou MFVideoInterlace_MixedInterlaceOrProgressive.<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | Si la <strong>valeur est true</strong>, le premier champ est répété. Si la valeur est <strong>false</strong> ou non définie, le premier champ n’est pas répété. | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | Si la <strong>valeur est true</strong>, l’exemple contient un champ unique. Si la <strong>valeur est false</strong>, l’exemple contient des champs entrelacés. | 




 

Le tableau suivant indique les indicateurs requis, facultatifs ou interdits, en fonction du type de média.



| Type de support         | Indicateur entrelacé                      | Indicateur BottomFieldFirst                    | Indicateur RepeatFirstField | Indicateur SingleField                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| Progressif        | Facultatif s’il est défini, doit avoir la **valeur false**. | Ne pas définir.                              | Ne pas définir.           | Ne pas définir.                          |
| Champs entrelacés | Facultatif Si cette propriété est définie, elle doit avoir la **valeur true**.  | Facultatif Si cette valeur est définie, doit correspondre au type de média. | Ne pas définir.           | Facultatif s’il est défini, doit avoir la **valeur false**. |
| Champs uniques      | Facultatif Si cette propriété est définie, elle doit avoir la **valeur true**.  | Obligatoire.                                | Ne pas définir.           | Affectez la valeur **true**.                     |
| Mixte              | Obligatoire.                            | Obligatoire.                                | Obligatoire.             | Facultatif s’il est défini, doit avoir la **valeur false**. |



 

Dans les cas où l’attribut est facultatif, le type de média définit déjà les informations. Il est possible de définir l’attribut pour qu’il corresponde, mais ce n’est pas obligatoire.

Par exemple, si le type de média est \_ progressif MFVideoInterlace, cela implique que toutes les trames dans le flux sont progressives. Par conséquent, vous pouvez définir l' **attribut \_ entrelacé MFSampleExtension** sur **false** ou conserver l’attribut unset.

## <a name="recommendations"></a>Recommandations

Cette section contient des recommandations pour différents types de contenu.

1. La vidéo est l’ensemble des trames progressives.

-   Définissez le type de média sur MFVideoInterlace \_ progressive.

-   Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **false** sur chaque frame.

-   Ne définissez pas les attributs **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** ou **MFSampleExtension \_ SingleField** .

2. La vidéo est l’ensemble des champs entrelacés avec la même dominante de champ. Les exemples contiennent des champs entrelacés.

-   Définissez le type de média sur MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.

-   Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **true** sur chaque frame.

-   Ne définissez pas l’attribut **MFSampleExtension \_ BottomFieldFirst** , ou définissez la valeur de chaque frame pour qu’elle corresponde au type de média.

-   Ne définissez pas l’attribut **MFSampleExtension \_ RepeatFirstField** , ou affectez-lui la valeur **false** pour chaque frame.

-   Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **false** pour chaque frame.

3. La vidéo contient une combinaison d’images entrelacées et progressives, avec des champs répétés et une dominante de champ variable (par exemple, DVD vidéo).

-   Définissez le type de média sur MFVideoInterlace \_ MixedInterlaceOrProgressive.

-   Sur chaque trame, définissez les attributs **MFSampleExtension \_ entrelacé**, **MFSampleExtension \_ BottomFieldFirst** et **MFSampleExtension \_ RepeatFirstField** .

-   Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **false** pour chaque frame.

4. La vidéo est entrelacée et les exemples contiennent des champs uniques.

-   Définissez le type de média sur MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.

-   Sur chaque trame, définissez l’attribut **MFSampleExtension \_ BottomFieldFirst** .

-   Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **true** sur chaque frame.

-   Ne définissez pas l’attribut **MFSampleExtension \_ RepeatFirstField** , ou affectez-lui la valeur **false** pour chaque frame.

-   Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **true** sur chaque frame.

La plupart des contenus vidéo appartiennent à l’une de ces catégories.

## <a name="mpeg-2-mappings"></a>Mappages MPEG-2

Pour le contenu MPEG-2, utilisez les mappages suivants pour convertir les indicateurs MPEG-2 en Media Foundation exemples d’attributs.

**structure d’image \_**



| Valeur         | Exemple d’attribut                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| frame         | **MFSampleExtension \_ SingleField**  =  **false**                                                                          |
| champ du haut \_    | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**<br/> |
| champ du bas \_ | **MFSampleExtension \_ SingleField**  =  **true**<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**<br/>  |



 

**Frame progressif \_**



| Valeur | Exemple d’attribut                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_ Entrelacé**  =  **true**  |
| 1     | **MFSampleExtension \_**  =  **False** entrelacé |



 

**champ supérieur en \_ \_ premier**



| Valeur | Exemple d’attribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ BottomFieldFirst**  =  **true**  |
| 1     | **MFSampleExtension \_ BottomFieldFirst**  =  **false** |



 

**répéter le \_ premier \_ champ**



| Valeur | Exemple d’attribut                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_ RepeatFirstField**  =  **false** |
| 1     | **MFSampleExtension \_ RepeatFirstField**  =  **true**  |



 

## <a name="single-field-samples"></a>Exemples de Single-Field

Si le type de média est MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower, cela signifie que chaque échantillon contient un champ unique. Toutefois, le type de média décrit le frame entier. Par conséquent, chaque mémoire tampon contient uniquement la moitié du nombre de lignes de champs fournies dans le type de média. Par exemple, si le type de média décrit la vidéo sous la forme 720 × 480, chaque champ contient 240 lignes de numérisation, et par conséquent, chaque mémoire tampon contient uniquement 240 lignes de pixels. Si vous écrivez un composant qui accepte des types de média avec des exemples à champ unique, vous devez prendre ce fait en compte lorsque vous accédez aux données dans la mémoire tampon.

La même règle s’applique à l’ouverture géométrique (attribut d'[ \_ \_ \_ ouverture géométrique MF MT](mf-mt-geometric-aperture-attribute.md) ) et à l’ouverture de l’affichage minimale (attribut d’ouverture d’affichage de l'[ \_ affichage MF MT \_ minimum \_ \_ ](mf-mt-minimum-display-aperture-attribute.md) ). Ces régions sont spécifiées en termes d’ensemble du cadre, et non des champs individuels.

## <a name="directshow-mappings"></a>DirectShow Mappages

dans DirectShow, les informations d’entrelacement par échantillon sont contenues dans le membre **dwTypeSpecificFlags** de la structure de **\_ \_ propriétés AM SAMPLE2** . Le tableau suivant présente les attributs équivalents pour Media Foundation.



| indicateur d’exemple de DirectShow              | Media Foundation l’exemple d’attribut                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| image de l' \_ \_ indicateur vidéo \_ entrelacé \_ | **MFSampleExtension \_ SingleField**  =  **false**.                                                                                                                                    |
| \_Indicateur de vidéo am \_ \_ champ1             | **MFSampleExtension \_**  =  **True** entrelacé.<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **false**.<br/> |
| \_Indicateur vidéo \_ am \_ champ2             | **MFSampleExtension \_**  =  **True** entrelacé.<br/> **MFSampleExtension \_ SingleField**  =  **true**.<br/> **MFSampleExtension \_ BottomFieldFirst**  =  **true**.<br/>  |
| \_indicateur vidéo \_ am \_ tissage              | **MFSampleExtension \_**  =  **False** entrelacé. (Cet indicateur indique que le pilote ne doit pas désentrelacer les deux champs.)                                                        |
| \_Indicateur vidéo \_ am \_ FIELD1FIRST        | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. Si le contenu est entrelacé et que l’indicateur AM \_ Video \_ Flag \_ FIELD1FIRST n’est pas présent, affectez la valeur **true** à cet attribut.        |
| champ de répétition de l' \_ indicateur vidéo am \_ \_ \_      | **MFSampleExtension \_ RepeatFirstField**  =  **true**. Si l' \_ indicateur de champ REPEAT de l’indicateur de vidéo am \_ \_ \_ n’est pas présent, affectez la valeur **false** à cet attribut.                                    |



 

si l’exemple DirectShow ne contient pas d’indicateurs, utilisez la valeur de **dwInterlaceFlags** à partir de la structure **VIDEOINFOHEADER2** :



| DirectShow l’indicateur entrelacé    | Media Foundation l’exemple d’attribut                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_**  =  **True** entrelacé.        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_ SingleField**  =  **true**.       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_ BottomFieldFirst**  =  **false**. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 




