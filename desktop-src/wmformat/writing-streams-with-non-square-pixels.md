---
title: écriture de Flux avec des Pixels Non carrés
description: écriture de Flux avec des Pixels Non carrés
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, écriture de flux vidéo
- Windows Media Format SDK, flux vidéo
- Windows Media Format SDK, pixels non carrés
- Windows Media Format SDK, pixels (non carré)
- ASF (Advanced Systems Format), écriture de flux vidéo
- ASF (format avancé des systèmes), écriture de flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- ASF (Advanced Systems Format), pixels non carrés
- ASF (format des systèmes avancés), pixels non carrés
- Format de systèmes avancés (ASF), pixels (non carrés)
- ASF (format des systèmes avancés), pixels (non carrés)
- écriture de flux vidéo
- flux vidéo, écriture
- flux vidéo, pixels non carrés
- pixels non carrés
- pixels (non carrés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b44df1e4b4ce3f2bf2cb0e1d795b4caf396b6396e3e70b68b9040ad9a5456f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657949"
---
# <a name="writing-streams-with-non-square-pixels"></a>écriture de Flux avec des Pixels Non carrés

il existe deux façons de créer des flux vidéo avec des pixels non carrés qui s’affichent correctement dans Lecteur Windows Media. La première technique consiste à définir des attributs au niveau du flux dans l’en-tête du fichier. La deuxième technique implique l’ajout d’une extension d’unité de données à un flux du profil, puis la définition d’une valeur pour celle-ci dans chaque exemple écrit.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Pour utiliser des attributs d’en-tête au niveau du flux pour définir les proportions de pixels

1.  Configurez l’objet Writer. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).
2.  Créez ou chargez un profil avec un ou plusieurs flux vidéo. Pour plus d’informations, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).
3.  Appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). (Appelez toujours cette méthode avant de définir des attributs d’en-tête.)
4.  Appelez **QueryInterface** pour obtenir l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) et appelez [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) à deux reprises pour ajouter [**AspectRatioX**](aspectratiox.md) et [**AspectRatioY**](aspectratioy.md) en tant qu’attributs de niveau flux du flux vidéo. Ces attributs sont des valeurs **DWORD** .
5.  Écrivez le fichier.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Pour utiliser les extensions d’unité de données pour définir les proportions de pixels

**Avant d’écrire :**

1.  Configurez l’objet Writer. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).
2.  Créez ou chargez un profil avec un ou plusieurs flux vidéo. Pour plus d’informations, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).
3.  Pour chaque flux (de n’importe quel type de média) dans le profil, appelez [**IWMStreamConfig :: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) pour spécifier un nom unique de votre choix. Ne donnez pas le même nom à deux flux.
4.  Utilisez [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) sur le flux vidéo pour ajouter une extension d’unité de données pour les proportions de pixels.
5.  Appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Écrivez le fichier.

**Lors de l’écriture :**

-   Pour chaque exemple, appelez [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) et spécifiez la \_ propriété WM SampleExtensionGUID \_ PixelAspectRatio, ainsi que la valeur correcte. Les valeurs de proportions sont écrites sous la forme de deux valeurs concaténées à deux chiffres. Par exemple, 16:9 est écrit sous la forme 1609 ou 0x0649. Il s’agit toujours d’une valeur de 2 octets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**pour lire et écrire des Flux vidéo avec des Pixels Non carrés**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




