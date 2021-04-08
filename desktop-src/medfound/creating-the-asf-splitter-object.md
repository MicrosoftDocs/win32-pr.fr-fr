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
# <a name="creating-the-asf-splitter-object"></a>Création de l’objet Splitter ASF

L’objet *séparateur* ASF est un objet de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format). Pour créer une nouvelle instance de l’objet Splitter ASF, appelez la fonction [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) . Cette fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) qui représente un objet Splitter vide.

Avant que le séparateur puisse commencer l’analyse, l’application doit initialiser le séparateur avec les informations de l’objet d’en-tête ASF. Pour initialiser le séparateur, appelez la méthode [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) . Cette méthode prend un pointeur vers l' [objet ASF ContentInfo](asf-contentinfo-object.md) qui contient les informations d’en-tête du fichier ASF à analyser. L’application doit initialiser l’objet ContentInfo avant de le passer au séparateur afin que les caractéristiques du fichier multimédia soient connues de l’application. La méthode **Initialize** de Splitter extrait les informations de flux de l’objet ContentInfo, telles que les numéros de flux, afin que le séparateur puisse analyser les paquets de données.

### <a name="example"></a>Exemple

L’exemple de code suivant montre comment créer un séparateur et l’initialiser avec un objet ContentInfo existant.


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
> Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séparateur ASF](asf-splitter.md)
</dt> </dl>

 

 



