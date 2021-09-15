---
description: Implémentation de IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implémentation de IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412223"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implémentation de IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

Plusieurs blocs de métadonnées existent souvent dans une image, chacun exposant différents types d’informations dans différents formats. dans le modèle WIC (Windows Imaging component), les gestionnaires de métadonnées sont des composants distincts qui, comme les décodeurs, sont détectables au moment de l’exécution. Chaque format de métadonnées a un gestionnaire distinct, et chacun de ces gestionnaires de métadonnées peut être utilisé avec tout format d’image qui prend en charge le format de métadonnées qu’il gère. Par conséquent, si votre format d’image prend en charge EXIF, XMP, IPTC ou un autre format, vous pouvez tirer parti des gestionnaires de métadonnées standard pour ces formats fournis avec WIC, et vous n’avez pas besoin d’écrire le vôtre. Bien entendu, si vous créez un nouveau format de métadonnées, vous devez écrire un gestionnaire de métadonnées pour celui-ci, qui sera découvert et appelé au moment de l’exécution comme les valeurs standard.

> [!Note]  
> Si votre format d’image est basé sur un conteneur TIFF (Tagged Image File Format) ou JPEG, vous n’avez pas besoin d’écrire de gestionnaires de métadonnées (sauf si vous développez un nouveau format de métadonnées propriétaire). Dans les conteneurs TIFF et JPEG, les blocs de métadonnées se trouvent dans IFD, et chaque conteneur a une structure IFD différente. WIC fournit des gestionnaires IFD pour ces deux formats de conteneur qui parcourent la structure IFD et délèguent aux gestionnaires de métadonnées standard pour accéder aux métadonnées qu’ils contiennent. Par conséquent, si votre format d’image est basé sur l’un de ces conteneurs, vous pouvez automatiquement tirer parti des gestionnaires IFD du WIC. Toutefois, si vous avez un format de conteneur propriétaire qui a sa propre structure de métadonnées de niveau supérieur unique, vous devez écrire un gestionnaire qui peut naviguer dans cette structure de niveau supérieur et déléguer aux gestionnaires de métadonnées appropriés, tout comme les gestionnaires IFD.)

 

De la même façon, WIC fournit une couche d’abstraction pour les applications qui leur permet de fonctionner avec tous les formats d’image de la même façon via un ensemble cohérent d’interfaces, WIC fournit une couche d’abstraction pour les auteurs de codec en ce qui concerne les formats de métadonnées. Comme indiqué précédemment, les auteurs de codec n’ont généralement pas besoin de travailler directement avec les différents formats de métadonnées qui peuvent être présents dans une image. Toutefois, chaque auteur de codec est chargé de fournir un moyen d’énumérer les blocs de métadonnées afin qu’un gestionnaire de métadonnées approprié puisse être découvert et instancié pour chaque bloc.

Vous devez implémenter cette interface sur votre classe de décodage au niveau de la trame. Vous devrez peut-être également l’implémenter sur votre classe de décodeur au niveau du conteneur si votre format d’image expose des métadonnées globales en dehors de toutes les trames d’image individuelles.

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) est identique à la méthode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) lors de l' [implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) retourne le nombre de blocs de métadonnées de niveau supérieur associés au frame.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) retourne un énumérateur que l’appelant peut utiliser pour énumérer les blocs de métadonnées dans le frame et lire leurs métadonnées. Pour implémenter cette méthode, vous devez créer un lecteur de métadonnées pour chaque bloc de métadonnées et implémenter un objet d’énumération qui énumère la collection de lecteurs de métadonnées. L’objet d’énumération doit implémenter [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) afin que vous puissiez le convertir en IEnumUnknown lorsque vous le retournez dans le paramètre *ppIEnumMetadata* .

Lors de l’implémentation de l’objet d’énumération, vous pouvez créer tous les lecteurs de métadonnées lorsque vous créez pour la première fois l’objet [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) ou lorsque vous créez l’objet d’énumération pour la première fois, ou vous pouvez les créer de manière différée à l’intérieur de l’implémentation de la méthode [IEnumUnknown :: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) . Dans de nombreux cas, il est plus efficace de les créer tardivement, mais dans l’exemple suivant, les lecteurs de bloc sont tous créés dans le constructeur pour économiser de l’espace.


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



Pour créer les lecteurs de métadonnées, vous utilisez la méthode [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) . Lors de l’appel de cette méthode, vous transmettez le GUID du format de conteneur dans le paramètre *guidContainerFormat* . Si vous avez une préférence de fournisseur pour un lecteur de métadonnées, vous pouvez transmettre le GUID de votre fournisseur préféré dans le paramètre *pGuidVendor* . Par exemple, si votre entreprise écrit des gestionnaires de métadonnées et que vous souhaitez utiliser la vôtre si elle est présente, vous pouvez transmettre le GUID de votre fournisseur. Dans la plupart des cas, vous devez simplement passer la **valeur null** et laisser le système sélectionner le lecteur de métadonnées approprié. Si vous demandez un fournisseur spécifique et que celui-ci dispose d’un lecteur de métadonnées installé sur l’ordinateur, WIC retourne le lecteur de ce fournisseur. Toutefois, si le fournisseur demandé ne dispose pas d’un lecteur de métadonnées installé sur l’ordinateur et si un lecteur de métadonnées approprié est disponible, ce lecteur est retourné même s’il ne provient pas du fournisseur préféré. S’il n’existe aucun lecteur de métadonnées sur l’ordinateur pour le type de métadonnées dans le bloc, la fabrique de composants retourne le gestionnaire de métadonnées inconnu, qui traite le bloc de métadonnées comme un objet BLOB (Binary Large Object) et désérialise le bloc de métadonnées du fichier sans aucune tentative d’analyse.

Pour le paramètre *dwOptions* , effectuez une opération or entre le [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) approprié et le [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)approprié. Le **WICPersistOptions** décrit comment votre conteneur est disposé. La valeur par défaut est Little endian.

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

Le [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) spécifie si vous souhaitez récupérer le UnknownMetadataHandler si aucun lecteur de métadonnées n’est trouvé sur l’ordinateur qui peut lire le format de métadonnées d’un bloc particulier. **WICMetadataCreationAllowUnknown** est la valeur par défaut, et vous devez toujours autoriser la création du UnknownMetadtataHandler. UnknownMetadataHandler traite les métadonnées non reconnues comme un objet BLOB. Il ne peut pas l’analyser, mais il l’écrit dans le flux en tant qu’objet BLOB et le rend intact quand il est réécrit dans le flux pendant l’encodage. Cela permet de créer en toute sécurité des gestionnaires de métadonnées pour les formats de métadonnées propriétaires ou de métadonnées qui ne sont pas fournis avec le système. Étant donné que les métadonnées sont conservées intactes, même si aucun gestionnaire n’est présent sur l’ordinateur qui les reconnaît, lorsqu’un gestionnaire de métadonnées approprié est installé ultérieurement, les métadonnées sont toujours présentes et peuvent être lues. Si vous n’autorisez pas la création du UnknownMetadataHandler, l’alternative ignore ou remplace les métadonnées non reconnues. Il s’agit d’une forme de perte de données.

> [!Note]  
> Si vous écrivez votre propre gestionnaire de métadonnées pour les métadonnées propriétaires, vous ne devez jamais inclure de références à ce qui se trouve en dehors du bloc de métadonnées lui-même. Même si le UnknownMetadataHandler conserve les métadonnées intactes, les métadonnées sont déplacées lors de la modification des fichiers et toutes les références à des éléments en dehors de son propre bloc ne seront plus valides lorsque cela se produit.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

Le paramètre *pIStream* est le flux réel que vous décodez. Avant de passer le flux, vous devez rechercher le début du bloc de métadonnées pour lequel vous demandez un lecteur. Le lecteur de métadonnées approprié pour le bloc de métadonnées à la position actuelle dans l' [IStream](/windows/desktop/api/objidl/nn-objidl-istream) est retourné dans le paramètre *ppiReader* .

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) retourne le lecteur de métadonnées à l’index demandé dans la collection.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Implémentation de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implémentation de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
