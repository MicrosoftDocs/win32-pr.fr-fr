---
description: utilisation de Windows Media avec les Services d’édition DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: utilisation de Windows Media avec les Services d’édition DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8c2e73fd4593a5f078c78e1e8290303b3574a314a504c4a555c46929361813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755929"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>utilisation de Windows Media avec les Services d’édition DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cette section décrit comment utiliser Windows contenu multimédia dans une application de [Services d’édition DirectShow](directshow-editing-services.md) (DES). Il existe deux scénarios principaux :

-   Éléments sources. un projet DES peut contenir des clips audio et vidéo de Windows fichiers multimédias.
-   Format cible. Windows Le média est un format idéal pour la sortie finale d’un projet de montage vidéo.

pour utiliser des fichiers multimédias Windows, l’application doit fournir un certificat logiciel, également appelé clé. Pour ce faire, il implémente un objet de fournisseur de clés. Le fournisseur de clé est un objet COM qui expose l’interface **IServiceProvider** . pour plus d’informations sur l’implémentation du fournisseur de clé, consultez [déverrouillage du kit de développement logiciel (SDK) Windows Media Format](unlocking-the-windows-media-format-sdk.md).

pour utiliser les Windows avec des fichiers multimédias, les objets des suivants requièrent la clé logicielle :

-   Moteur de rendu, pour l’aperçu ou l’écriture de fichiers.
-   Objet MediaDet, pour récupérer des images vidéo ou des types de média à partir de fichiers ASF.
-   \[! Précieuse\]  
    > n’utilisez pas le moteur de rendu intelligent pour lire ou écrire Windows fichiers multimédias. Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).

     

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



pour utiliser Windows clips source de média dans un projet DES, appelez simplement **IObjectWithSite :: setsite** sur le moteur de rendu avec un pointeur vers votre fournisseur de clés.

pour plus d’informations sur l’écriture de Windows fichiers multimédias, consultez [écriture d’un fichier multimédia Windows dans DES](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



