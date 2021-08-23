---
description: Cette rubrique explique comment écrire un gestionnaire de propriétés de shell personnalisé pour une source de média Microsoft Media Foundation.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Fournisseurs de métadonnées personnalisés pour les fichiers multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777599"
---
# <a name="custom-metadata-providers-for-media-files"></a>Fournisseurs de métadonnées personnalisés pour les fichiers multimédias

Cette rubrique explique comment écrire un gestionnaire de propriétés de shell personnalisé pour une source de média Microsoft Media Foundation.

> [!Note]  
> Pour obtenir des informations générales sur les fournisseurs de métadonnées dans Media Foundation, consultez [Metadata Media](media-metadata.md). Cette rubrique décrit les gestionnaires de propriétés de Shell. elle ne décrit pas l’interface de métadonnées de la version 1, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).

 

Les métadonnées sont étroitement liées au format du fichier. Dans Media Foundation, les formats de fichier sont représentés par des sources multimédias. Si vous souhaitez prendre en charge les métadonnées pour un format qui n’est pas pris en charge en mode natif dans Media Foundation, vous devez implémenter une source de média personnalisée avec un gestionnaire de propriétés. Le gestionnaire de propriétés permet au système de propriétés de Shell de lire et d’écrire des métadonnées efficacement.

Un gestionnaire de propriétés est un objet COM qui implémente les interfaces suivantes :

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Le cas échéant, elle peut également exposer l’interface suivante :

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Si le système de propriétés de l’interpréteur de commandes doit obtenir les métadonnées d’un fichier, il appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire de propriétés, puis appelle les méthodes de lecture et d’écriture appropriées sur l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Le pipeline Media Foundation utilise un mécanisme légèrement différent, car le pipeline obtient le gestionnaire de propriétés directement à partir de la source du média. Au lieu d’appeler [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire de propriétés, le pipeline appelle [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la source du média, comme décrit dans la rubrique [fournisseurs de métadonnées de l’interpréteur](shell-metadata-providers.md)de commandes.

Pour créer un gestionnaire de propriétés personnalisées, procédez comme suit :

-   Implémentez l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) pour exposer [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Le GUID du service est le **\_ service de \_ gestionnaire \_ de propriétés MF**.
-   Si la source du média est utilisée à distance, elle doit également exposer l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) par le biais de la méthode **QueryInterface** de la source du média, en plus de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).
-   Pour mettre le gestionnaire de propriétés à la disposition du système de propriétés de l’interpréteur de commandes, inscrivez la DLL du gestionnaire de propriétés comme décrit dans la rubrique [inscription et distribution de gestionnaires de propriétés](../properties/prophand-reg-dist.md).
-   La source du média est inscrite séparément, comme décrit dans [gestionnaires de modèles et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Astuces d’implémentation

Pour obtenir la liste des clés de propriété de métadonnées, consultez [Propriétés de métadonnées pour les fichiers multimédias](metadata-properties-for-media-files.md).

Les gestionnaires de propriétés doivent être rapides ; ils doivent fournir un accès efficace en lecture et en écriture aux métadonnées. (Considérez que l’interpréteur de commandes peut récupérer des métadonnées de centaines de fichiers.) Par conséquent, n’appelez pas [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) à partir de votre gestionnaire de propriétés. La fonction **MFStartup** introduit la latence de démarrage, car elle crée plusieurs threads de file d’attente de travail et alloue de la mémoire globale.

Dans une implémentation classique, le gestionnaire de propriétés et la source du média partagent une partie du même code d’analyse. Toutefois, une source de média utilise des appels [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) asynchrones pour les e/s, tandis que le gestionnaire de propriétés utilise l’interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Media Foundation fournit un objet d’assistance qui encapsule un flux basé sur **IStream** et l’expose en tant que flux **IMFByteStream** . Pour créer le wrapper, appelez [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).

Lors de la mise à jour des métadonnées, il est recommandé d’écrire les données directement dans le flux d’origine. Cette recommandation diffère du comportement de *copie sur écriture* de la plupart des gestionnaires de propriétés, dans lesquels une copie des données est modifiée. Les fichiers multimédias peuvent être très volumineux. par conséquent, la copie sur écriture est généralement trop lente pour une implémentation efficace. Pour désactiver la copie en écriture, définissez le paramètre de Registre **ManualSafeSave** , comme décrit dans la rubrique [inscription et distribution de gestionnaires de propriétés](../properties/prophand-reg-dist.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Métadonnées de média](media-metadata.md)
</dt> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Écriture d’une source de média personnalisée](writing-a-custom-media-source.md)
</dt> </dl>

 

 
