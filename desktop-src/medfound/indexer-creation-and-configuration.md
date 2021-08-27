---
description: Cette rubrique fournit des informations sur la création de l’objet indexeur par défaut fourni par Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Création et configuration de l’indexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061199"
---
# <a name="indexer-creation-and-configuration"></a>Création et configuration de l’indexeur

L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format). Cette rubrique fournit des informations sur la création de l’objet indexeur par défaut fourni par Media Foundation.

Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

**Pour créer et initialiser l’indexeur ASF**

1.  Appelez la fonction [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) pour recevoir un pointeur [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) vers l’objet indexeur.
2.  Appelez [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) pour spécifier le mode de lecture ou d’écriture pour l’objet indexeur. Par défaut, l’indexeur est configuré pour la recherche vers l’avant.

    

    | Utilisation                       | Indicateur                                           |
    |---------------------------|------------------------------------------------|
    | Lecture (recherche anticipée) | Zéro (valeur par défaut)                                 |
    | Lecture (inversée) | **\_indexeur MFASF \_ lu \_ pour \_ REVERSEPLAYBACK** |
    | Écriture                   | \_indexer MFASF \_ écrire \_ un nouvel \_ index              |

    

     

    > [!Note]  
    > La même instance de l’indexeur ne peut pas être utilisée à la fois pour la lecture et l’écriture. Vous devez configurer l’indexeur pour l’un ou l’autre.

     

3.  Appelez [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) pour initialiser l’indexeur en spécifiant le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) de l’objet ContentInfo qui décrit le fichier à écrire ou à lire. L’objet ContentInfo contient des informations qui constituent l' [objet d’en-tête ASF](asf-file-structure.md). L’objet indexeur requiert un objet ContentInfo valide avant de générer ou de lire les entrées d’index d’un fichier ASF.

L’exemple de code suivant montre comment une application peut créer et initialiser l’objet indexeur pour qu’il fonctionne avec un contenu ASF spécifique. L’objet ContentInfo représente l’objet d’en-tête ASF ; le contenu est passé en tant que flux d’octets.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexeur ASF](asf-index-object.md)
</dt> <dt>

[Utilisation de l’indexeur pour rechercher dans un fichier ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Utilisation de l’indexeur pour écrire un nouvel index](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



