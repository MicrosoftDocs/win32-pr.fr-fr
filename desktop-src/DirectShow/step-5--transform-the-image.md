---
description: Étape 5.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Étape 5. Transformer l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209728"
---
# <a name="step-5-transform-the-image"></a>Étape 5. Transformer l’image

Il s’agit de l’étape 5 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

Le filtre en amont remet des échantillons de médias au filtre de transformation en appelant la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée du filtre de transformation. Pour traiter les données, le filtre de transformation appelle la méthode de **transformation** , qui est virtuelle pure. Les classes **CTransformFilter** et **CTransInPlaceFilter** utilisent deux versions différentes de cette méthode :

-   [**CTransformFilter :: Transform**](ctransformfilter-transform.md) accepte un pointeur vers l’exemple d’entrée et un pointeur vers l’exemple de sortie. Avant que le filtre appelle la méthode, il copie les exemples de propriétés de l’exemple d’entrée dans l’exemple de sortie, y compris les horodatages.
-   [**CTransInPlaceFilter :: Transform**](ctransinplacefilter-transform.md) accepte un pointeur vers l’exemple d’entrée. Le filtre modifie les données sur place.

Si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple en aval. Pour ignorer un frame, renvoyez la \_ valeur false. En cas d’erreur de diffusion en continu, retourne un code d’échec.

L’exemple suivant montre comment l’encodeur RLE peut implémenter cette méthode. Votre propre implémentation peut varier considérablement, en fonction de ce que fait votre filtre.


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



Cet exemple suppose que EncodeFrame est une méthode privée qui implémente l’encodage RLE. L’algorithme d’encodage lui-même n’est pas décrit ici ; Pour plus d’informations, consultez la rubrique « compression bitmap » dans la documentation du kit de développement Platform SDK.

Tout d’abord, l’exemple appelle [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) pour récupérer les adresses des mémoires tampons sous-jacentes. Elle les transmet à la méthode EncoderFrame privée. Ensuite, il appelle [**IMediaSample :: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) pour spécifier la longueur des données encodées. Le filtre en aval a besoin de ces informations pour pouvoir gérer correctement la mémoire tampon. Enfin, la méthode appelle [**IMediaSample :: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) pour définir l’indicateur d’image clé sur **true**. L’encodage de longueur d’exécution n’utilise pas d’images Delta, donc chaque frame est une image clé. Pour les images Delta, définissez la valeur sur **false**.

Les autres problèmes que vous devez prendre en compte sont les suivants :

-   Horodatages. La classe **CTransformFilter** horodate l’exemple de sortie avant d’appeler la méthode **Transform** . Elle copie les valeurs d’horodatage de l’exemple d’entrée, sans les modifier. Si votre filtre doit modifier les horodatages, appelez [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) sur l’exemple de sortie.
-   Modifications de format. Le filtre amont peut modifier les formats Mid-Stream en attachant un type de média à l’exemple. Avant cela, il appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche d’entrée de votre filtre. Dans la classe **CTransformFilter** , cela entraîne un appel à **CheckInputType** suivi de **CheckTransform**. Le filtre en aval peut également modifier les types de médias à l’aide du même mécanisme. Dans votre propre filtre, il y a deux choses à surveiller :

    -   Assurez-vous que **QueryAccept** ne retourne pas les fausses acceptations.
    -   Si votre filtre accepte les modifications de format, vérifiez-les à l’intérieur de la méthode **Transform** en appelant [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Si cette méthode retourne \_ la valeur OK, votre filtre doit répondre au changement de format.

    Pour plus d’informations, consultez [modifications de format dynamique](dynamic-format-changes.md).

-   Thèmes. Dans **CTransformFilter** et **CTransInPlaceFilter**, le filtre de transformation remet les exemples de sortie de façon synchrone à l’intérieur de la méthode **Receive** . Le filtre ne crée pas de threads de travail pour traiter les données. En règle générale, il n’y a aucune raison pour qu’un filtre de transformation crée des threads de travail.

Suivant : [étape 6. Ajoutez la prise en charge de COM](step-6--add-support-for-com.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



