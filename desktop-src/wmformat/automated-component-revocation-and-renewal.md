---
title: Révocation et renouvellement de composants automatisés
description: Révocation et renouvellement de composants automatisés
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK, révocation et renouvellement automatisés
- Windows Media Format SDK, révocation
- Windows Media Format SDK, renouvellement
- gestion des droits numériques (DRM), révocation et renouvellement automatisés
- DRM (gestion des droits numériques), révocation et renouvellement automatisés
- gestion des droits numériques (DRM), révocation
- DRM (gestion des droits numériques), révocation
- gestion des droits numériques (DRM), renouvellement
- DRM (gestion des droits numériques), renouvellement
- API étendues du client DRM, révocation et renouvellement automatisés
- API étendues clientes, révocation et renouvellement automatisés
- API étendues du client DRM, révocation
- API étendues clientes, révocation
- API étendues du client DRM, renouvellement
- API étendues clientes, renouvellement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316001"
---
# <a name="automated-component-revocation-and-renewal"></a>Révocation et renouvellement de composants automatisés

Les applications logicielles ou les composants considérés comme compromis peuvent être révoqués par Microsoft. L’API étendue du client Windows Media Format fournit un mécanisme pour la révocation et le renouvellement automatisés des composants.

Les composants révoqués sont répertoriés dans une liste de révocation de certificats publiée par Microsoft. Lorsqu’un composant est révoqué, son certificat est ajouté à la liste de révocation de certificats, et l’objet BLOB des informations de révocation \_ est mis à jour sur les serveurs Microsoft.

Pour effectuer une révocation et un renouvellement automatisés lorsqu’un utilisateur tente de traiter le contenu protégé par DRM Windows Media, votre application doit effectuer les opérations suivantes :

1.  Extrayez la \_ version infos Rev de la licence. Le \_ numéro de version des informations Rev se trouve à l’emplacement suivant dans une licence XMR :
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  Comparez le \_ numéro de version des informations Rev de la licence avec le \_ numéro de version d’informations Rev dans le magasin local en appelant la méthode [**IWMDRMSecurity :: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .
3.  Si la \_ version infos Rev n’est pas à jour, appelez la méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , en passant l' \_ \_ \_ \_ indicateur d’actualisation de la sécurité WMDRM dans le paramètre *dwFlags* .
4.  Récupérez la liste de révocation de certificats à partir du magasin local en appelant la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
5.  Analyser la liste de révocation et vérifier les révocations DRM Windows Media. Pour plus d’informations, consultez vérification de la [révocation des certificats](checking-certificate-revocation.md).
6.  S’il existe des révocations DRM Windows Media :
    1.  Créez un activateur de contenu pour renouveler les composants révoqués en appelant la méthode [**IWMDRMSecurity :: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .
    2.  Appelez **IMFContentEnabler :: AutomaticEnable** qui dirige l’utilisateur vers une URL qui contient des informations de renouvellement de composant. Cette méthode est documentée dans le [Kit de développement logiciel (SDK) Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > Vous devez clarifier ce processus à l’utilisateur à l’aide d’une déclaration de confidentialité, car le processus de mise à jour envoie des informations à partir de l’ordinateur client vers un site Web Microsoft.

         

    3.  Si possible, l’utilisateur renouvelle le composant à partir de l’URL, soit automatiquement, soit en suivant les instructions spécifiques. Dans certaines situations, le composant ne peut pas être renouvelé.
    4.  Essayez d’accéder à nouveau au contenu jusqu’à ce qu’il n’y ait plus de révocations, sinon le processus est interrompu pour une raison quelconque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](drm-programming-guide.md)
</dt> </dl>

 

 