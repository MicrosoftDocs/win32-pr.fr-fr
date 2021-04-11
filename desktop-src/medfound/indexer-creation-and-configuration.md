---
description: Cette rubrique fournit des informations sur la création de l’objet indexeur par défaut fourni par Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Création et configuration de l’indexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203873"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="10dbf-103">Création et configuration de l’indexeur</span><span class="sxs-lookup"><span data-stu-id="10dbf-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="10dbf-104">L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="10dbf-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="10dbf-105">Cette rubrique fournit des informations sur la création de l’objet indexeur par défaut fourni par Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="10dbf-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="10dbf-106">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="10dbf-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="10dbf-107">**Pour créer et initialiser l’indexeur ASF**</span><span class="sxs-lookup"><span data-stu-id="10dbf-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="10dbf-108">Appelez la fonction [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) pour recevoir un pointeur [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) vers l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="10dbf-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="10dbf-109">Appelez [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) pour spécifier le mode de lecture ou d’écriture pour l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="10dbf-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="10dbf-110">Par défaut, l’indexeur est configuré pour la recherche vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="10dbf-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="10dbf-111">Utilisation</span><span class="sxs-lookup"><span data-stu-id="10dbf-111">Use</span></span>                       | <span data-ttu-id="10dbf-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="10dbf-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="10dbf-113">Lecture (recherche anticipée)</span><span class="sxs-lookup"><span data-stu-id="10dbf-113">Reading (forward seeking)</span></span> | <span data-ttu-id="10dbf-114">Zéro (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10dbf-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="10dbf-115">Lecture (inversée)</span><span class="sxs-lookup"><span data-stu-id="10dbf-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="10dbf-116">**\_indexeur MFASF \_ lu \_ pour \_ REVERSEPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="10dbf-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="10dbf-117">Écriture</span><span class="sxs-lookup"><span data-stu-id="10dbf-117">Writing</span></span>                   | <span data-ttu-id="10dbf-118">\_indexer MFASF \_ écrire \_ un nouvel \_ index</span><span class="sxs-lookup"><span data-stu-id="10dbf-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="10dbf-119">La même instance de l’indexeur ne peut pas être utilisée à la fois pour la lecture et l’écriture.</span><span class="sxs-lookup"><span data-stu-id="10dbf-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="10dbf-120">Vous devez configurer l’indexeur pour l’un ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="10dbf-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="10dbf-121">Appelez [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) pour initialiser l’indexeur en spécifiant le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) de l’objet ContentInfo qui décrit le fichier à écrire ou à lire.</span><span class="sxs-lookup"><span data-stu-id="10dbf-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="10dbf-122">L’objet ContentInfo contient des informations qui constituent l' [objet d’en-tête ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="10dbf-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="10dbf-123">L’objet indexeur requiert un objet ContentInfo valide avant de générer ou de lire les entrées d’index d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="10dbf-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="10dbf-124">L’exemple de code suivant montre comment une application peut créer et initialiser l’objet indexeur pour qu’il fonctionne avec un contenu ASF spécifique.</span><span class="sxs-lookup"><span data-stu-id="10dbf-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="10dbf-125">L’objet ContentInfo représente l’objet d’en-tête ASF ; le contenu est passé en tant que flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="10dbf-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="10dbf-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10dbf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10dbf-127">Indexeur ASF</span><span class="sxs-lookup"><span data-stu-id="10dbf-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="10dbf-128">Utilisation de l’indexeur pour rechercher dans un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="10dbf-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="10dbf-129">Utilisation de l’indexeur pour écrire un nouvel index</span><span class="sxs-lookup"><span data-stu-id="10dbf-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



