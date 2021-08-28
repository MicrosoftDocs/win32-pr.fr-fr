---
description: Encodage vidéo entrelacé
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Encodage vidéo entrelacé (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15269aca3f2878504fef56c62b1a1d70ecd89295c237164ba864b15aaae371d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724389"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Encodage vidéo entrelacé (Microsoft Media Foundation)

Les données vidéo destinées à être utilisées avec les ordinateurs sont généralement *progressifs*, ce qui signifie que chaque image est encodée sous la forme d’une image unique. Certains appareils, comme les téléviseurs, n’affichent pas de frame en même temps, mais sous forme de deux images. L’une des images, ou champs, contient toutes les lignes paires numérotées. L’autre champ contient les données de toutes les lignes impaires numérotées. La vidéo encodée avec plusieurs champs par trame est appelée entrelacée, car elle est rendue en basculant entre le champ pair et le champ impair.

dans le passé, le contenu vidéo entrelacé était toujours déentrelacé avant l’encodage avec le codec Windows Media Video. toutefois, à partir de Windows Media 9 Series, l’encodeur vidéo prend en charge la compression de contenu entrelacé sans avoir d’abord à le convertir en progressif. La conservation de l’entrelacement dans un fichier encodé est importante si le contenu est toujours rendu sur un écran entrelacé, tel qu’une télévision. cette fonctionnalité est de plus en plus importante, car elle prend en charge la réplication de contenu multimédia Windows sur des lecteurs de DVD, des boîtiers décodeurs et d’autres appareils électroniques à la base.

le moyen le plus simple pour encoder et distribuer de la vidéo entrelacée est de développer votre application à l’aide du kit de développement logiciel (SDK) Windows Media Format et de stocker le contenu dans des fichiers ASF. Les informations entrelacées sur les frames sont transmises au codec à l’aide d’extensions d’unité de données, qui fonctionnent bien pour le contenu ASF, mais sont un peu plus délicates à prendre en charge dans d’autres conteneurs. Pour plus d’informations sur les extensions d’unité de données, consultez [utilisation des extensions d’unité de données](usingdataunitextensions.md).

La prise en charge de l’encodage entrelacé implique deux étapes principales : l’obtention des informations de trame à l’encodeur et la transmission des informations à l’application de rendu. Ces étapes sont décrites dans les paragraphes suivants.

## <a name="interlaced-video-and-the-encoder"></a>Vidéo entrelacée et encodeur

La première étape de l’encodage d’une vidéo avec entrelacement conservé consiste à configurer l’encodeur pour encoder les champs entrelacés. Pour ce faire, affectez la valeur **true** à la propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) . Cela prépare l’encodeur pour recevoir des échantillons entrelacés. Chaque exemple d’entrée doit contenir les deux champs.

Chaque exemple que vous traitez avec l’encodeur après l’activation de l’encodage entrelacé doit avoir une extension d’unité de données attachée. Les exemples sans l’extension d’unité de données attendue sont considérés comme progressifs. Le GUID identifiant l’extension est D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. les valeurs transmises par les objets du kit de développement logiciel (SDK) Windows Media Format sont définies dans le tableau suivant.



| Valeur      | Description                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Spécifie que l’échantillon est encodé avec le champ inférieur en premier. Cette valeur est significative uniquement lorsqu’elle est associée à la valeur entrelacée. |
| 0x00000040 | Spécifie que l’échantillon est encodé avec le champ supérieur en premier. Cette valeur est significative uniquement lorsqu’elle est associée à la valeur entrelacée.    |
| 0x00000080 | Spécifie que l’échantillon est entrelacé. Il s’agit de la seule valeur qui est significative pour le codec DMOs.                                    |



 

L’une des deux premières valeurs est toujours combinée avec 0x80 à l’aide d' **une opération de bits or avant** d’être définie sur l’exemple. Toutefois, l’encodeur vérifie uniquement 0x80 et ignore le reste de l’extension. Si l’extension identifie l’échantillon comme entrelacé, l’encodeur maintient l’entrelacement de l’échantillon dans le flux compressé et incorpore un indicateur d’indication dans le flux afin que le décodeur puisse identifier des frames entrelacés. Chaque échantillon entrelacé est marqué, de sorte que le contenu source qui est une combinaison de profondeurs et entrelacés peut être encodé dans un flux.

l’objet enregistreur SDK Windows Media Format contient les extensions d’unité de données de type de contenu dans les exemples qu’il écrit dans la section de données du conteneur ASF pour une utilisation au moment du rendu.

## <a name="reading-and-rendering-interlaced-video"></a>Lecture et rendu de la vidéo entrelacée

Le décodeur identifie les échantillons entrelacés en fonction de l’indicateur défini dans le flux par l’encodeur. Par défaut, le décodeur réentrelace les exemples et fournit des sorties progressives. L’application de lecteur peut configurer le décodeur pour traiter les sorties avec entrelacement géré en définissant la propriété de [ \_ \_ désentrelacement de décodeur MFPKEY](mfpkey-decoder-deinterlacingproperty.md) .

La difficulté de la lecture vidéo entrelacée se produit après que le décodeur a effectué les exemples. Le convertisseur (carte vidéo ou puce dans un appareil) ne peut pas afficher correctement le contenu vidéo sans savoir quel champ est. dans les applications utilisant le kit de développement logiciel (SDK) de Format de média Windows, l’extension d’unité de données de type de contenu est récupérée à partir des exemples non compressés et peut être transmise à l’appareil.

Lorsque vous utilisez les objets codec directement, aucun de ces transferts de données n’est automatique. Vous devez implémenter la prise en charge de l’extension des unités de données, à la fois dans vos objets de mémoire tampon et dans le conteneur que vous utilisez pour votre contenu encodé. La plupart des types courants de conteneurs multimédias (comme AVI) ne prennent pas en charge les métadonnées au niveau de l’échantillon. Vous pouvez implémenter votre propre système pour stocker les données dans le fichier et les associer à des échantillons individuels, mais seul un lecteur personnalisé est en mesure de le récupérer.

> [!Note]  
> Si vous affectez la **valeur true** à la propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) et que vous n’envoyez pas d’exemples avec l’extension d’unité de données Content-type attachée, l’encodeur risque de se bloquer. Définissez l’encodeur pour l’encodage entrelacé uniquement si vous avez des échantillons entrelacés à remettre.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



