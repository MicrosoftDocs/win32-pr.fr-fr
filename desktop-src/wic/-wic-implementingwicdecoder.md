---
description: 'En savoir plus sur : implémentation d’un décodeur WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implémentation d’un décodeur WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866762"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implémentation d’un décodeur WIC-Enabled


L’implémentation d’un décodeur WIC (Windows Imaging Component) requiert l’écriture de deux classes. Les interfaces sur ces classes correspondent directement aux responsabilités de décodeur décrites dans la section [décodage](-wic-howwicworks.md) du [fonctionnement du composant de création d’images Windows](-wic-howwicworks.md).

L’une des classes fournit des services au niveau du conteneur et implémente l’interface [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) . Si votre format d’image prend en charge les métadonnées au niveau du conteneur, vous devez également implémenter l’interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) sur cette classe. Il est recommandé de prendre en charge l’interface [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sur le décodeur et l’encodeur afin de prendre en charge une meilleure expérience utilisateur.

L’autre classe que vous allez implémenter fournit des services au niveau de la trame et effectue le décodage réel des bits d’image pour chaque frame dans le conteneur. Cette classe implémente l’interface [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) et l’interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) . Si vous écrivez un décodeur pour un format brut, vous implémentez également l’interface [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) sur cette classe. Outre les interfaces requises, il est vivement recommandé d’implémenter l’interface [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) sur cette classe pour bénéficier des meilleures performances possibles pour votre format d’image.

L’un des objets fournis par WIC est le [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). Vous utilisez fréquemment l’interface [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) sur cet objet pour créer différents composants. Étant donné qu’il est fréquemment utilisé, vous devez conserver une référence à celui-ci en tant que propriété de membre sur vos classes de décodeur et d’encodeur.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Fonctionnement du composant de création d’images Windows](-wic-howwicworks.md)
</dt> <dt>

[Interfaces de décodeur](-wic-decoderinterfaces.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble de l’encodage](-wic-creating-encoder.md)
</dt> </dl>

 

 



