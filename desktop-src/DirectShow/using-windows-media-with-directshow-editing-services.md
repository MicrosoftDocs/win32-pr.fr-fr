---
description: Utilisation de Windows Media avec les services de modification DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Utilisation de Windows Media avec les services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539786"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Utilisation de Windows Media avec les services de modification DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cette section décrit comment utiliser du contenu Windows Media dans une application des [services de modification DirectShow](directshow-editing-services.md) . Il existe deux scénarios principaux :

-   Éléments sources. Un projet DES peut contenir des clips audio et vidéo de fichiers Windows Media.
-   Format cible. Windows Media est un format idéal pour la sortie finale d’un projet de montage vidéo.

Pour travailler avec des fichiers Windows Media, l’application doit fournir un certificat logiciel, également appelé clé. Pour ce faire, il implémente un objet de fournisseur de clés. Le fournisseur de clé est un objet COM qui expose l’interface **IServiceProvider** . Pour plus d’informations sur l’implémentation du fournisseur de clé, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).

Pour utiliser DES avec des fichiers Windows Media, les objets DES suivants nécessitent la clé logicielle :

-   Moteur de rendu, pour l’aperçu ou l’écriture de fichiers.
-   Objet MediaDet, pour récupérer des images vidéo ou des types de média à partir de fichiers ASF.
-   \[! Précieuse\]  
    > N’utilisez pas le moteur de rendu intelligent pour lire ou écrire des fichiers Windows Media. Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).

     

Pour attribuer à un objet la clé logicielle, interrogez cet objet pour l’interface **IObjectWithSite** et appelez **IObjectWithSite :: sets** avec un pointeur vers votre fournisseur de clés. Par exemple, le code suivant fournit la clé logicielle au moteur de rendu :


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Pour utiliser des clips source Windows Media dans un projet DES, appelez simplement **IObjectWithSite :: SetSite** sur le moteur de rendu avec un pointeur vers votre fournisseur de clés.

Pour plus d’informations sur l’écriture de fichiers Windows Media, consultez [écriture d’un fichier Windows Media dans des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



