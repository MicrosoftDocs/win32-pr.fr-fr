---
description: Cette rubrique présente la configuration requise pour la création de gestionnaires de métadonnées personnalisés pour le composant WIC (Windows Imaging Component), y compris les lecteurs et les enregistreurs de métadonnées.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Vue d’ensemble de l’extensibilité des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203657"
---
# <a name="metadata-extensibility-overview"></a>Vue d’ensemble de l’extensibilité des métadonnées

Cette rubrique présente la configuration requise pour la création de gestionnaires de métadonnées personnalisés pour le composant WIC (Windows Imaging Component), y compris les lecteurs et les enregistreurs de métadonnées. Il aborde également la configuration requise pour l’extension de la détection des composants runtime WIC pour inclure vos gestionnaires de métadonnées personnalisés.

Cette rubrique contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Introduction](#introduction)
-   [Création d’un lecteur de métadonnées](#creating-a-metadata-reader)
    -   [Interface IWICMetadataReader](#iwicmetadatareader-interface)
    -   [Interface IWICPersistStream](#iwicpersiststream-interface)
    -   [Interface IWICStreamProvider](#iwicstreamprovider-interface)
-   [Création d’un enregistreur de métadonnées](#creating-a-metadata-writer)
    -   [Interface IWICMetadataWriter](#iwicmetadatawriter-interface)
    -   [Interface IWICPersistStream](#iwicpersiststream-interface)
    -   [Interface IWICStreamProvider](#iwicstreamprovider-interface)
-   [Installation et inscription d’un gestionnaire de métadonnées](#installing-and-registering-a-metadata-handler)
    -   [Clés de Registre du gestionnaire de métadonnées](#metadata-handler-registry-keys)
    -   [Lecteurs de métadonnées](#metadata-readers)
    -   [Enregistreurs de métadonnées](#metadata-writers)
    -   [Signature d’un gestionnaire de métadonnées](#signing-a-metadata-handler)
-   [Considérations spéciales](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Gestionnaires 8BIM](#8bim-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez avoir une connaissance approfondie de WIC, de ses composants et de ses métadonnées pour les images. Pour plus d’informations sur les métadonnées WIC, consultez [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md). Pour plus d’informations sur les composants WIC, consultez [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Introduction

Comme indiqué dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md), il existe souvent plusieurs blocs de métadonnées dans une image, chacun exposant différents types d’informations dans différents formats de métadonnées. Pour interagir avec un format de métadonnées incorporé dans une image, une application doit utiliser un gestionnaire de métadonnées approprié. WIC fournit plusieurs gestionnaires de métadonnées (les lecteurs et les enregistreurs de métadonnées) qui vous permettent de lire et d’écrire des types de métadonnées spécifiques, tels que EXIF ou XMP.

Outre les gestionnaires natifs fournis, WIC fournit des API qui vous permettent de créer de nouveaux gestionnaires de métadonnées qui participent à la détection des composants d’exécution de WIC. Cela permet aux applications qui utilisent WIC de lire et d’écrire vos formats de métadonnées personnalisés.

Les étapes suivantes permettent à vos gestionnaires de métadonnées de participer à la découverte des métadonnées au moment de l’exécution du WIC.

-   Implémentez une classe de gestionnaire de lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) qui expose les interfaces WIC requises pour lire votre format de métadonnées personnalisé. Cela permet aux applications WIC de lire votre format de métadonnées de la même façon qu’elles lisent des formats de métadonnées natifs.
-   Implémentez une classe de gestionnaire d’écriture de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) qui expose les interfaces WIC requises pour l’encodage de votre format de métadonnées personnalisé. Cela permet aux applications basées sur WIC de sérialiser votre format de métadonnées dans des formats d’image pris en charge.
-   Signez et inscrivez numériquement vos gestionnaires de métadonnées. Cela permet de découvrir vos gestionnaires de métadonnées au moment de l’exécution en faisant correspondre le modèle d’identification dans le Registre avec le modèle incorporé dans le fichier image.

## <a name="creating-a-metadata-reader"></a>Création d’un lecteur de métadonnées

Le principal accès aux blocs de métadonnées au sein d’un codec s’effectue via l’interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) que chaque codec WIC implémente. Cette interface énumère chacun des blocs de métadonnées incorporés dans un format d’image afin que le gestionnaire de métadonnées approprié puisse être découvert et instancié pour chaque bloc. Les blocs de métadonnées qui ne sont pas reconnus par WIC sont considérés comme inconnus et sont définis en tant que GUID CLSID \_ WICUnknownMetadataReader. Pour que votre format de métadonnées soit reconnu par WIC, vous devez créer une classe qui implémente trois interfaces : [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)et [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Si votre format de métadonnées a des restrictions qui rendent certaines méthodes des interfaces requises inappropriées, ces méthodes doivent retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>Interface IWICMetadataReader

L’interface [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) doit être implémentée lors de la création d’un lecteur de métadonnées. Cette interface fournit l’accès aux éléments de métadonnées sous-comprises dans le flux de données d’un format de métadonnées.

Le code suivant illustre la définition de l’interface du lecteur de métadonnées telle que définie dans le fichier wincodecsdk. idl.

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

La méthode **GetMetadataFormat** retourne le GUID de votre format de métadonnées.

La méthode **GetMetadataHandlerInfo** retourne une interface [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) qui fournit des informations sur votre gestionnaire de métadonnées. Cela comprend des informations telles que les formats d’image qui prennent en charge le format de métadonnées et si votre lecteur de métadonnées requiert l’accès au flux de métadonnées complet.

La méthode **GetCount** retourne le nombre d’éléments de métadonnées individuels (y compris les blocs de métadonnées incorporés) trouvés dans le flux de métadonnées.

La méthode **GetValueByIndex** retourne un élément de métadonnées par une valeur d’index. Cette méthode permet aux applications de parcourir chaque élément de métadonnées dans un bloc de métadonnées. Le code suivant montre comment une application peut utiliser cette méthode pour récupérer chaque élément de métadonnées dans un bloc de métadonnées.


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



La méthode **GetValue** récupère un élément de métadonnées spécifique par schéma et/ou ID. Cette méthode est similaire à la méthode **GetValueByIndex** , à ceci près qu’elle récupère un élément de métadonnées ayant un schéma ou un ID spécifique.

La méthode **GetEnumerator** retourne un énumérateur de chaque élément de métadonnées dans le bloc de métadonnées. Cela permet aux applications d’utiliser un énumérateur pour naviguer dans votre format de métadonnées.

Si votre format de métadonnées n’a pas de notion de schémas pour les éléments de métadonnées, le GetValue... les méthodes doivent ignorer cette propriété. Toutefois, si votre format prend en charge les noms de schéma, vous devez anticiper une valeur **null** .

Si un élément de métadonnées est un bloc de métadonnées incorporé, créez un gestionnaire de métadonnées à partir du sous-flux du contenu incorporé et retournez le nouveau gestionnaire de métadonnées. Si aucun lecteur de métadonnées n’est disponible pour le bloc imbriqué, instanciez et retournez un lecteur de métadonnées inconnu. Pour créer un lecteur de métadonnées pour le bloc incorporé, appelez les méthodes **CreateMetadataReaderFromContainer** ou **CreateMetadataReader** de la fabrique de composants, ou appelez la fonction [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .

Si le flux de métadonnées contient du contenu de poids fort (Big-endian), le lecteur de métadonnées est responsable de la permutation des valeurs de données qu’il traite. Il est également chargé d’informer les lecteurs de métadonnées imbriqués qu’ils utilisent le flux de données Big-endian. Toutefois, toutes les valeurs doivent être retournées au format Little endian.

Implémentez la prise en charge de la navigation dans les espaces de noms en prenant en charge les requêtes où l’ID d’élément de métadonnées est un `VT_CLSID` (Guid) correspondant à un format de métadonnées. Si un lecteur de métadonnées imbriqué pour ce format est identifié lors de l’analyse, il doit être retourné. Cela permet aux applications d’utiliser un lecteur de requêtes de métadonnées pour rechercher votre format de métadonnées.

Lors de l’obtention d’un élément de métadonnées par ID, vous devez utiliser la [fonction PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) pour forcer l’ID dans le type attendu. Par exemple, le lecteur IFD convertit un ID en type `VT_UI2` pour qu’il coïncide avec le type de données d’un ID de balise IFD UShort. Le type d’entrée et le type attendu doivent tous deux être [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) pour ce faire. Ce n’est pas obligatoire, mais cette contrainte simplifie le code qui appelle le lecteur pour rechercher des éléments de métadonnées.

### <a name="iwicpersiststream-interface"></a>Interface IWICPersistStream

L’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hérite de **IPersistStream** et fournit des méthodes supplémentaires pour l’enregistrement et le chargement d’objets à l’aide de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

Le code suivant illustre la définition de l’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) comme défini dans le fichier wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

La méthode **LoadEx** fournit à votre lecteur de métadonnées un flux de données contenant votre bloc de métadonnées. Votre lecteur analyse ce flux pour accéder aux éléments de métadonnées sous-jacents. Votre lecteur de métadonnées est initialisé avec un sous-flux positionné au début du contenu de métadonnées brutes. Si votre lecteur ne requiert pas le flux complet, le sous-flux est limité dans la plage au contenu du bloc de métadonnées ; dans le cas contraire, le flux de métadonnées complet est fourni avec la position définie au début de votre bloc de métadonnées.

La méthode **SaveEx** est utilisée par les enregistreurs de métadonnées pour sérialiser votre bloc de métadonnées. Quand **SaveEx** est utilisé dans un lecteur de métadonnées, il doit retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>Interface IWICStreamProvider

L’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permet à votre lecteur de métadonnées de fournir des références à son flux de contenu, de fournir des informations sur le flux et d’actualiser les versions mises en cache du flux.

Le code suivant illustre la définition de l’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) comme défini dans le fichier wincodecsdk. idl.

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

La méthode **GetStream** récupère une référence à votre flux de métadonnées. Le point de départ du flux que vous renvoyez doit être réinitialisé à la position de début. Si votre format de métadonnées requiert un accès complet au flux, la position de départ doit être le début de votre bloc de métadonnées.

La méthode **GetPersistOptions** retourne les options actuelles du flux à partir de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

La méthode **GetPreferredVendorGUID** retourne le GUID du fournisseur du lecteur de métadonnées.

La méthode **RefreshStream** actualise le flux de métadonnées. Cette méthode doit appeler **LoadEx** avec un flux **null** pour tous les blocs de métadonnées imbriqués. Cela est nécessaire, car les blocs de métadonnées imbriqués et leurs éléments peuvent ne plus exister, en raison de la modification sur place.

## <a name="creating-a-metadata-writer"></a>Création d’un enregistreur de métadonnées

Un enregistreur de métadonnées est un type de gestionnaire de métadonnées qui fournit un moyen de sérialiser un bloc de métadonnées vers une image, ou à l’extérieur d’un frame individuel si le format d’image le prend en charge. L’accès principal aux enregistreurs de métadonnées au sein d’un codec s’effectue par le biais de l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que chaque encodeur WIC implémente. Cette interface permet aux applications d’énumérer chacun des blocs de métadonnées incorporés dans une image afin que le writer de métadonnées approprié puisse être découvert et instancié pour chaque bloc de métadonnées. Les blocs de métadonnées qui n’ont pas de writer de métadonnées correspondant sont considérés comme inconnus et sont définis en tant que GUID CLSID \_ WICUnknownMetadataReader. Pour permettre aux applications compatibles WIC de sérialiser et d’écrire votre format de métadonnées, vous devez créer une classe qui implémente les interfaces suivantes : [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)et [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Si votre format de métadonnées a des restrictions qui rendent certaines méthodes des interfaces requises inappropriées, ces méthodes doivent retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>Interface IWICMetadataWriter

L’interface [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) doit être implémentée par votre générateur de métadonnées. En outre, étant donné que **IWICMetadataWriter** hérite de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), vous devez également implémenter toutes les méthodes de **IWICMetadataReader**. Étant donné que les deux types de gestionnaires nécessitent le même héritage d’interface, vous pouvez créer une seule classe qui fournit des fonctionnalités de lecture et d’écriture.

Le code suivant illustre la définition de l’interface du writer de métadonnées telle que définie dans le fichier wincodecsdk. idl.

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

La méthode **SetValue** écrit l’élément de métadonnées spécifié dans le flux de métadonnées.

La méthode **SetValueByIndex** écrit l’élément de métadonnées spécifié dans l’index spécifié dans le flux de métadonnées. L’index ne fait pas référence à l’ID, mais à la position de l’élément dans le bloc de métadonnées.

La méthode **RemoveValue** supprime l’élément de métadonnées spécifié du flux de métadonnées.

La méthode **RemoveValueByIndex** supprime l’élément de métadonnées au niveau de l’index spécifié du flux de métadonnées. Après la suppression d’un élément, il est prévu que les éléments de métadonnées restants occupent l’index libéré si l’index n’est pas le dernier index. Il est également prévu que le nombre change une fois que l’élément a été supprimé.

Le générateur de métadonnées est chargé de convertir les éléments [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en structure sous-jacente requise par votre format. Toutefois, à la différence du lecteur de métadonnées, les types VARIANT ne doivent normalement pas être forcés à des types différents, car l’appelant indique spécifiquement le type de données à utiliser.

Votre enregistreur de métadonnées doit valider tous les éléments de métadonnées dans le flux d’image, y compris les valeurs masquées ou non reconnues. Cela comprend les blocs de métadonnées imbriqués inconnus. Toutefois, il incombe à l’encodeur de définir tous les éléments de métadonnées critiques avant de lancer l’opération d’enregistrement.

Si le flux de métadonnées contient du contenu de poids fort, le générateur de métadonnées est responsable de la permutation des valeurs de données qu’il traite. Il est également chargé d’informer tous les enregistreurs de métadonnées imbriqués qu’ils utilisent un flux de données Big-endian lorsqu’ils sont enregistrés.

Implémentez la prise en charge de la création et de la suppression des espaces de noms en prenant en charge les opérations Set et Remove sur les éléments de métadonnées avec un type `VT_CLSID` (Guid) correspondant à un format de métadonnées. Le générateur de métadonnées appelle la fonction [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) pour incorporer correctement le contenu du générateur de métadonnées imbriqué dans le writer de métadonnées parent.

Si votre format de métadonnées prend en charge l’encodage sur place, vous êtes chargé de gérer le remplissage requis. Pour plus d’informations sur l’encodage sur place, consultez [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md) et [vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md).

### <a name="iwicpersiststream-interface"></a>Interface IWICPersistStream

L’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hérite de **IPersistStream** et fournit des méthodes supplémentaires pour l’enregistrement et le chargement d’objets à l’aide de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

Le code suivant illustre la définition de l’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) comme défini dans le fichier wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

La méthode **LoadEx** fournit votre gestionnaire de métadonnées avec un flux de données contenant votre bloc de métadonnées.

La méthode **SaveEx** sérialise les métadonnées dans un flux. Si le flux fourni est le même que le flux d’initialisation, vous devez effectuer un encodage sur place. Si l’encodage sur place est pris en charge, cette méthode doit retourner WINCODEC \_ Err \_ TOOMUCHMETADATA lorsque le remplissage est insuffisant pour effectuer un encodage sur place. Si l’encodage sur place n’est pas pris en charge, cette méthode doit retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

La méthode **IPersistStream :: GetSizeMax** doit être implémentée et doit retourner la taille exacte du contenu des métadonnées qui serait écrit lors de l’enregistrement suivant.

La méthode **IPersistStream :: IsDirty** doit être implémentée si le writer de métadonnées est initialisé par le biais d’un flux, afin qu’une image puisse déterminer de manière fiable si son contenu a changé.

Si votre format de métadonnées prend en charge les blocs de métadonnées imbriqués, votre générateur de métadonnées doit déléguer aux rédacteurs de métadonnées imbriqués la sérialisation de son contenu lors de l’enregistrement dans un flux.

### <a name="iwicstreamprovider-interface"></a>Interface IWICStreamProvider

L’implémentation de l’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) pour un générateur de métadonnées est identique à celle d’un lecteur de métadonnées. Pour plus d’informations, consultez la section création d’un lecteur de métadonnées dans ce document.

## <a name="installing-and-registering-a-metadata-handler"></a>Installation et inscription d’un gestionnaire de métadonnées

Pour installer un gestionnaire de métadonnées, vous devez fournir l’assembly du gestionnaire et l’inscrire dans le registre système. Vous pouvez choisir le mode et le moment de remplissage des clés de registre.

> [!Note]  
> Pour des raisons de lisibilité, les GUID hexadécimaux réels ne sont pas affichés dans les clés de registre indiquées dans les sections suivantes de ce document. Pour rechercher la valeur hexadécimale d’un nom convivial spécifié, consultez les fichiers wincodec. idl et wincodecsdk. idl.

 

### <a name="metadata-handler-registry-keys"></a>Clés de Registre du gestionnaire de métadonnées

Chaque gestionnaire de métadonnées est identifié par un CLSID unique, et chaque gestionnaire est requis pour inscrire son CLSID sous le GUID de l’ID de catégorie du gestionnaire de métadonnées. L’ID de catégorie de chaque type de gestionnaire est défini dans wincodec. idl ; le nom d’ID de catégorie pour Readers est CATID \_ WICMetadataReader et le nom d’ID de catégorie pour les Writers est CATID \_ WICMetadataWriter.

Chaque gestionnaire de métadonnées est identifié par un CLSID unique, et chaque gestionnaire est requis pour inscrire son CLSID sous le GUID de l’ID de catégorie du gestionnaire de métadonnées. L’ID de catégorie de chaque type de gestionnaire est défini dans wincodec. idl ; le nom d’ID de catégorie pour Readers est CATID \_ WICMetadataReader et le nom d’ID de catégorie pour les Writers est CATID \_ WICMetadataWriter.

> [!Note]  
> Dans les listes de clés de Registre suivantes, {Reader CLSID} fait référence au CLSID unique que vous fournissez pour votre lecteur de métadonnées. {Writer CLSID} fait référence au CLSID unique que vous fournissez pour votre générateur de métadonnées. {Handler CLSID} fait référence au CLSID du lecteur, au CLSID du writer, ou aux deux, selon les gestionnaires que vous fournissez. {Container GUID} fait référence à l’objet conteneur (format d’image ou format de métadonnées) qui peut contenir le bloc de métadonnées.

 

Les clés de Registre suivantes inscrivent votre gestionnaire de métadonnées avec les autres gestionnaires de métadonnées disponibles :

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

En plus d’inscrire vos gestionnaires dans leurs catégories respectives, vous devez également inscrire des clés supplémentaires qui fournissent des informations spécifiques au gestionnaire. Les lecteurs et les enregistreurs partagent des exigences de clé de Registre similaires. La syntaxe suivante montre comment inscrire un gestionnaire. Le gestionnaire de lecteur et le gestionnaire d’écriture doivent être enregistrés de cette manière, à l’aide de leurs CLSID respectifs :

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>Lecteurs de métadonnées

L’inscription des lecteurs de métadonnées comprend également des clés qui décrivent comment le lecteur peut être incorporé dans un format de conteneur. Un format de conteneur peut être un format d’image tel que TIFF ou JPEG. Il peut également s’agir d’un autre format de métadonnées, tel qu’un bloc de métadonnées IFD. Les formats de conteneur d’images pris en charge en mode natif sont répertoriés dans wincodec. idl. chaque format de conteneur d’images est défini en tant que GUID avec un nom commençant par le GUID \_ ContainerFormat. Les formats de conteneur de métadonnées pris en charge en mode natif sont répertoriés dans wincodecsdk. idl. chaque format de conteneur de métadonnées est défini en tant que GUID avec un nom commençant par le GUID \_ MetadataFormat.

Les clés suivantes inscrivent un conteneur que le lecteur de métadonnées prend en charge, ainsi que les données nécessaires à la lecture de ce conteneur. Chaque conteneur pris en charge par le lecteur doit être inscrit de cette façon.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

La clé de modèle décrit le modèle binaire qui est utilisé pour faire correspondre le bloc de métadonnées au lecteur. Lors de la définition d’un modèle pour votre lecteur de métadonnées, il doit être suffisamment fiable pour qu’une correspondance positive signifie que le lecteur de métadonnées peut comprendre les métadonnées du bloc de métadonnées en cours de traitement.

La clé DataOffset décrit l’offset fixe des métadonnées à partir de l’en-tête de bloc. Cette clé est facultative et, si elle n’est pas spécifiée, signifie que les métadonnées réelles ne peuvent pas être localisées à l’aide d’un décalage fixe par rapport à l’en-tête de bloc.

### <a name="metadata-writers"></a>Enregistreurs de métadonnées

L’inscription de l’enregistreur de métadonnées comprend également des clés qui décrivent comment écrire l’en-tête précédant le contenu de métadonnées incorporé dans un format de conteneur. Comme avec le lecteur, un format de conteneur peut être un format d’image ou un autre bloc de métadonnées.

Les clés suivantes inscrivent un conteneur pris en charge par le writer de métadonnées, ainsi que les données nécessaires à l’écriture de l’en-tête et des métadonnées. Chaque conteneur pris en charge par le writer doit être inscrit de cette façon.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

La clé WriteHeader décrit le modèle binaire de l’en-tête de bloc de métadonnées à écrire. Ce modèle binaire coïncide avec la clé de modèle de lecteur du format de métadonnées.

La clé WriteOffset décrit l’offset fixe à partir de l’en-tête de bloc auquel les métadonnées doivent être écrites. Cette clé est facultative et, si elle n’est pas spécifiée, signifie que les métadonnées réelles ne doivent pas être écrites avec l’en-tête.

### <a name="signing-a-metadata-handler"></a>Signature d’un gestionnaire de métadonnées

Tous les gestionnaires de métadonnées doivent être signés numériquement pour participer au processus de découverte du WIC. WIC ne chargera aucun gestionnaire qui n’est pas signé par une autorité de certification approuvée. Pour plus d’informations sur la signature numérique, consultez [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="special-considerations"></a>Considérations spéciales

Les sections suivantes incluent des informations supplémentaires que vous devez prendre en compte lors de la création de vos propres gestionnaires de métadonnées.

### <a name="propvariants"></a>PROPVARIANTS

WIC utilise un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) pour représenter un élément de métadonnées à la fois pour la lecture et l’écriture. Un PROPVARIANT fournit un type de données et une valeur de données pour un élément de métadonnées utilisé dans un format de métadonnées. En tant qu’auteur d’un gestionnaire de métadonnées, vous disposez d’une grande flexibilité sur la façon dont les données sont stockées dans le format de métadonnées et sur la façon dont les données sont représentées dans un bloc de métadonnées. Le tableau suivant fournit des instructions pour vous aider à déterminer le type de PROPVARIANT approprié à utiliser dans différentes situations.



| Le type de métadonnées est...          | Utiliser le type PROPVARIANT      | Propriété PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vide ou inexistant.       | VT \_ vide                 | Non applicable.                                                                                                                                                                                                                                                                |
| Non défini.                   | \_objet BLOB VT                  | Utilisez la propriété BLOB pour définir la taille et le pointeur sur l’objet BLOB alloué à l’aide de CoTaskMemAlloc.                                                                                                                                                                           |
| Bloc de métadonnées.            | VT \_ inconnu               | Ce type utilise la propriété punkVal.                                                                                                                                                                                                                                           |
| Tableau de types.           | VT \_ Vector \| VT \_ {type}  | Utilisez la propriété ca {type} pour définir le nombre et le pointeur sur le tableau alloué à l’aide de CoTaskMemAlloc.                                                                                                                                                                            |
| Tableau de blocs de métadonnées. | \_variante VT Vector \| VT \_ | Utilisez la propriété capropvar pour définir le tableau de variants.                                                                                                                                                                                                                       |
| Valeur rationnelle signée.     | Le \_ i8 VT                    | Utilisez la propriété hVal pour définir la valeur. Définissez le mot de poids fort sur le dénominateur et le mot de poids faible sur le numérateur.                                                                                                                                                                |
| Valeur rationnelle.            | \_UI8 VT                   | Utilisez la propriété uhVal pour définir la valeur. Définissez HighPart sur le dénominateur et LowPart sur le numérateur. Notez que LowPart est un entier non signé. Le numérateur doit être converti d’un int non signé en int pour garantir que le bit de signe est préservé s’il est présent. |



 

Pour éviter la redondance dans la représentation d’éléments de tableau, n’utilisez pas de tableaux sécurisés ; Utilisez uniquement des tableaux simples. Cela réduit le travail qu’une application doit effectuer lors de l’interprétation des types [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Évitez d’utiliser `VT_BYREF` et de stocker les valeurs inline dans la mesure du possible. `VT_BYREF` est inefficace pour les petits types (communs aux éléments de métadonnées) et ne fournit pas d’informations sur la taille.

Avant d’utiliser un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), appelez toujours **PropVariantInit** pour initialiser la valeur. Lorsque vous avez terminé avec le PROPVARIANT, appelez toujours **PropVariantClear** pour libérer toute mémoire allouée pour la variable.

### <a name="8bim-handlers"></a>Gestionnaires 8BIM

Lors de l’écriture d’un gestionnaire de métadonnées pour un bloc de métadonnées 8BIM, vous devez utiliser une signature qui encapsule la signature 8BIM et l’ID. Par exemple, le lecteur de métadonnées 8BIMIPTC natif fournit les informations de Registre suivantes pour la découverte des lecteurs :

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

Le lecteur 8BIMIPTC a un modèle inscrit de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. Les quatre premiers octets (0x38, 0x42, 0x49, 0x4D) sont la signature 8BIM, et les deux derniers octets (0x04, 0x04) sont l’ID de l’enregistrement IPTC.

Ainsi, pour écrire un lecteur de métadonnées 8BIM pour les informations de résolution, vous avez besoin d’un modèle inscrit de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. Là encore, les quatre premiers octets (0x38, 0x42, 0x49, 0x4D) sont la signature 8BIM. Toutefois, les deux derniers octets (0x03, 0xED) sont l’ID des informations de résolution tel que défini par le format PSD.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Comment : recoder une image JPEG avec des métadonnées](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
