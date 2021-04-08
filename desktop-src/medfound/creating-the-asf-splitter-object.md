---
description: Création de l’objet Splitter ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Création de l’objet Splitter ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861813"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="be0a8-103">Création de l’objet Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="be0a8-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="be0a8-104">L’objet *séparateur* ASF est un objet de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="be0a8-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="be0a8-105">Pour créer une nouvelle instance de l’objet Splitter ASF, appelez la fonction [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="be0a8-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="be0a8-106">Cette fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) qui représente un objet Splitter vide.</span><span class="sxs-lookup"><span data-stu-id="be0a8-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="be0a8-107">Avant que le séparateur puisse commencer l’analyse, l’application doit initialiser le séparateur avec les informations de l’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="be0a8-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="be0a8-108">Pour initialiser le séparateur, appelez la méthode [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="be0a8-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="be0a8-109">Cette méthode prend un pointeur vers l' [objet ASF ContentInfo](asf-contentinfo-object.md) qui contient les informations d’en-tête du fichier ASF à analyser.</span><span class="sxs-lookup"><span data-stu-id="be0a8-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="be0a8-110">L’application doit initialiser l’objet ContentInfo avant de le passer au séparateur afin que les caractéristiques du fichier multimédia soient connues de l’application.</span><span class="sxs-lookup"><span data-stu-id="be0a8-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="be0a8-111">La méthode **Initialize** de Splitter extrait les informations de flux de l’objet ContentInfo, telles que les numéros de flux, afin que le séparateur puisse analyser les paquets de données.</span><span class="sxs-lookup"><span data-stu-id="be0a8-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="be0a8-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="be0a8-112">Example</span></span>

<span data-ttu-id="be0a8-113">L’exemple de code suivant montre comment créer un séparateur et l’initialiser avec un objet ContentInfo existant.</span><span class="sxs-lookup"><span data-stu-id="be0a8-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="be0a8-114">Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="be0a8-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="be0a8-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be0a8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be0a8-116">Séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="be0a8-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



