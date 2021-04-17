---
description: Implémentation de IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implémentation de IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530268"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implémentation de IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

La classe d’encodage au niveau de la trame implémente cette interface pour exposer tous les blocs de métadonnées et demander le writer de métadonnées approprié pour chaque bloc. Si votre format d’image prend en charge les métadonnées globales, en dehors de tout Frame individuel, vous devez également implémenter cette interface sur la classe de codeur au niveau du conteneur. Pour une présentation plus détaillée des gestionnaires de métadonnées, reportez-vous à la section du [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) dans la section sur l’implémentation d’un décodeur de WIC-Enabled.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) utilise un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) pour initialiser le writer de bloc. Vous pouvez récupérer le **IWICMetadataBlockReader** à partir du décodeur qui a décodé l’image.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Étant donné que l’initialisation du [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) avec un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instancie un writer de métadonnées pour chaque lecteur de métadonnées exposé par l’objet **IWICMetadataBlockReader** , l’application n’a pas besoin de demander explicitement un writer pour chaque bloc de métadonnées.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) retourne l’objet [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) pour le nième bloc de métadonnées, où n est la valeur passée dans le paramètre *nIndex* . Si aucun enregistreur de métadonnées inscrit ne peut gérer le type de métadonnées dans le bloc nième, la fabrique de composants retourne le gestionnaire de métadonnées inconnu, qui traite le bloc de métadonnées comme un objet BLOB (Binary Large Object). Il le sérialise comme un flux binaire sans tenter de l’analyser.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permet à un appelant d’ajouter un nouveau générateur de métadonnées. Cela est obligatoire si une application souhaite ajouter des métadonnées d’un format différent de celui des blocs de métadonnées existants. Par exemple, une application peut souhaiter ajouter des métadonnées XMP. S’il n’existe aucun bloc de métadonnées XMP existant, l’application doit instancier un enregistreur de métadonnées XMP et utiliser la méthode **AddWriter** pour l’inclure dans la collection de Writers de métadonnées.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) est utilisé pour ajouter un enregistreur de métadonnées à un index spécifique dans la collection. Si un enregistreur de métadonnées existe actuellement à cet index, le nouveau doit le remplacer.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) est utilisé pour supprimer un enregistreur de métadonnées de la collection.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Installation et inscription du CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



