---
title: Entrées de flux arbitraires et précompressés
description: Entrées de flux arbitraires et précompressés
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), entrées de flux arbitraires
- ASF (format de systèmes avancés), entrées de flux arbitraires
- profils, entrées de flux arbitraires
- codecs, entrées de flux arbitraires
- ASF (Advanced Systems Format), entrées de flux précompressées
- ASF (format des systèmes avancés), entrées de flux précompressées
- profils, entrées de flux précompressés
- codecs, entrées de flux précompressés
- entrées de flux précompressées
- entrées de flux arbitraires
- flux, entrées de flux arbitraires
- flux, entrées de flux précompressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106513514"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Entrées de flux arbitraires et précompressés

Seules les entrées qui doivent être compressées par l’un des codecs Windows Media ont plusieurs entrées possibles. Les autres types d’entrées possibles sont les entrées arbitraires et les entrées précompressées. La configuration requise pour les formats d’entrée pour ces types est décrite dans cette section.

## <a name="arbitrary-stream-inputs"></a>Entrées de flux arbitraires

Les entrées des types de flux arbitraires sont les mêmes que les formats de flux décrits dans le profil. Vous ne devez pas avoir à définir des formats d’entrée pour ces types.

## <a name="precompressed-stream-inputs"></a>Entrées de flux précompressées

Lors de la copie d’un flux d’un fichier vers un autre, vous transmettez des exemples qui sont déjà compressés. Dans ce cas, vous devez affecter la **valeur null** à l’objet de propriétés d’entrée pour informer le writer qu’il n’a pas besoin de valider les données que vous passez. Pour définir le format d’entrée sur **null**, appelez [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) et transmettez **null** comme deuxième paramètre. Lors de l’appel de cette méthode avec un paramètre **null** , vous devez effectuer l’appel avant d’appeler [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Lorsque vous utilisez des flux précompressés, vous devez copier manuellement les informations du codec dans l’en-tête du fichier avant d’écrire. Pour obtenir les informations du codec, appelez [**IWMHeaderInfo2 :: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) et [**IWMHeaderInfo2 :: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) pour énumérer les codecs associés au fichier dans le lecteur. Sélectionnez les informations du codec qui correspondent à la configuration du flux du flux précompressé. Définissez ensuite les informations du codec dans le writer en appelant [**IWMHeaderInfo3 :: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), en passant les informations obtenues à partir du lecteur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> </dl>

 

 




