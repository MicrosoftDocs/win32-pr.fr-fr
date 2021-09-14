---
title: Pour distribuer des exemples compressés avec le lecteur asynchrone
description: Pour distribuer des exemples compressés avec le lecteur asynchrone
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- ASF (Advanced Systems Format), livrant des exemples compressés
- ASF (format avancé des systèmes), diffusion d’exemples compressés
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), exemples compressés
- ASF (Advanced Systems Format), exemples compressés
- lecteurs asynchrones, diffusion d’exemples compressés
- lecteurs asynchrones, exemples compressés
- exemples compressés, diffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293802"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Pour distribuer des exemples compressés avec le lecteur asynchrone

Le lecteur asynchrone peut fournir des échantillons compressés à partir de flux dans des fichiers ASF. Les applications fournissent généralement des exemples compressés lors de la copie d’un flux d’un fichier vers un autre. Il n’est pas recommandé de recompresser les données qui ont été reconstruites à partir d’un flux compressé, car les données sont perdues dans le processus d’encodage. Les médias numériques qui ont été compressés plusieurs fois auront une baisse notable de la qualité.

le kit de développement logiciel (SDK) Windows Media Format ne fournit aucune méthode pour décoder les données après leur extraction à partir d’un fichier ASF. Si vous recevez des exemples compressés et que vous souhaitez les décompresser ultérieurement, vous devrez fournir votre propre code pour ce faire. Une façon de contourner cette limitation consiste à écrire les exemples compressés dans un nouveau fichier ASF, puis à les relire dans des exemples normaux et non compressés.

Pour recevoir des exemples compressés avec le lecteur asynchrone, procédez comme suit.

1.  Implémentez le rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . Ce rappel est fondamentalement identique dans la fonction de [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , à ceci près qu’il fournit des échantillons par numéro de flux et que les exemples sont toujours compressés.
2.  Avant de commencer la lecture, obtenez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
3.  Configurez le lecteur pour remettre des exemples compressés pour le flux souhaité en appelant [**IWMReaderAdvanced :: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Répétez l’étape 3 pour chaque flux pour lequel l’exemple de remise compressé est souhaité.

> [!Note]  
> Les flux d’images ne sont pas valides pour la remise du flux compressé. Si vous copiez un flux d’image d’un fichier vers un autre, il ne fonctionnera pas dans le nouveau fichier. Pour copier un flux d’image à partir d’un fichier vers un fichier, récupérez les exemples de flux d’image par numéro de sortie et incluez-les dans le nouveau fichier comme si vous incluiez un nouveau flux d’image.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




