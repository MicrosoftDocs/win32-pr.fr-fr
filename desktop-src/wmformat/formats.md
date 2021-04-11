---
title: Formats
description: Formats
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, entrées
- Windows Media Format SDK, flux
- Windows Media Format SDK, sorties
- Windows Media Format SDK, formats
- ASF (Advanced Systems Format), entrées
- ASF (format des systèmes avancés), entrées
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- ASF (Advanced Systems Format), sorties
- ASF (format des systèmes avancés), sorties
- Formats ASF (Advanced Systems Format), formats
- ASF (format des systèmes avancés), formats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310785"
---
# <a name="formats"></a>Formats

Les informations contenues dans un format décrivent tout ce que vous devez savoir sur un type de média particulier. Chaque format a un type majeur, tel que audio ou vidéo, et peut avoir un sous-type. Les formats contiennent des informations différentes en fonction du type principal. Les formats audio et vidéo requièrent bien plus d’informations que d’autres types.

Tout comme les objets du kit de développement logiciel (SDK) de format Windows Media différencient les numéros d’entrée, les numéros de flux et les numéros de sortie (consultez [entrées, flux et sorties](inputs-streams-and-outputs.md)), il existe des différences importantes entre les formats d’entrée, les formats de flux et les formats de sortie. Ces différences sont décrites ici :

## <a name="input-formats"></a>Formats d’entrée

Un format d’entrée décrit les médias numériques que vous transmettez à l’objet enregistreur. Si un flux de données d’un fichier ASF est compressé à l’aide d’un codec, le codec prend en charge uniquement certains formats d’entrée. Lorsque vous utilisez les codecs vidéo et Windows Media Audio, vous pouvez énumérer les formats d’entrée pris en charge à l’aide de l’objet Writer. Lors de l’écriture d’un fichier, vous êtes responsable de la sélection d’un format d’entrée qui correspond à votre média d’entrée.

Bien que le format de média d’entrée doive être pris en charge par le codec destiné à compresser les données, certains paramètres de format d’entrée n’ont pas besoin de correspondre au format de flux. Par exemple, le format d’entrée d’un flux vidéo peut avoir une taille de trame différente de celle définie dans le format de flux. Dans ce cas, le codec effectue des conversions.

## <a name="stream-formats"></a>Formats de flux

Un format de flux décrit la forme du support tel qu’il est stocké dans le fichier ASF. Le format de flux est le format décrit dans le profil et peut être ou non le même que le format d’entrée et le format de sortie. Si un codec est utilisé pour compresser les données dans un flux, le format de flux est différent des formats d’entrée et de sortie.

Lorsque vous utilisez les codecs vidéo et Windows Media Audio, vous devez obtenir une liste des formats de flux pris en charge à partir du codec pour vous assurer que vous n’essayez pas de spécifier un format non pris en charge par le code. Certains paramètres de mise en forme, tels que la taille et la profondeur de couleur d’une image vidéo, doivent être configurés manuellement une fois le format du codec récupéré.

## <a name="output-formats"></a>Formats de sortie

Un format de sortie décrit les supports numériques que le lecteur (ou lecteur synchrone) remet à votre application. Si un flux de fichier ASF est compressé à l’aide d’un codec, le codec prend en charge uniquement certains formats de sortie. Lorsque vous utilisez les codecs Windows Media Audio et vidéo, vous pouvez énumérer les formats de sortie pris en charge à l’aide de l’objet Reader. Chacun des codecs Windows Media a un format de sortie par défaut, mais vous pouvez sélectionner n’importe quel format de sortie pris en charge pour l’exemple de remise.

Bien que le format de média de sortie doit être pris en charge par le codec qui a compressé les données, certains paramètres de format de sortie n’ont pas besoin de correspondre au format de flux. Par exemple, le format de sortie d’un flux vidéo peut avoir une taille de trame différente de celle définie dans le format de flux. Dans ce cas, le codec effectue des conversions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> </dl>

 

 




