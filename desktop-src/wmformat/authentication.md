---
title: Authentification (kit de développement logiciel (SDK) Windows Media format 11)
description: Authentification
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, authentification
- Windows Media Format SDK, authentification réseau
- ASF (Advanced Systems Format), authentification
- ASF (format des systèmes avancés), authentification
- ASF (Advanced Systems Format), authentification réseau
- ASF (format des systèmes avancés), authentification réseau
- Authentification
- authentification réseau, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512137"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Authentification (kit de développement logiciel (SDK) Windows Media format 11)

L’objet lecteur peut gérer les défis liés à l’authentification réseau, y compris l’authentification Digest et l’authentification NTLM. Dans certains cas, l’application doit fournir les informations d’identification de l’utilisateur par le biais d’une interface de rappel :

-   Authentification Digest : l’application doit implémenter l’interface **IWMCredentialCallback** , comme décrit plus loin dans cette rubrique.
-   Authentification NTLM : le lecteur répond automatiquement avec les informations d’identification d’ouverture de session de l’utilisateur. Si l’utilisateur actuel est autorisé à se connecter au serveur, l’application n’a rien à faire. Si l’utilisateur n’a pas d’autorisation, l’application doit implémenter l’interface **IWMCredentialCallback** .

    > [!Note]  
    > Windows Media Services version 4,1 ne prend pas en charge l’authentification NTLM par le biais d’un serveur proxy. L’authentification NTLM requiert plusieurs échanges client-serveur sur la même connexion, et la version 4,1 ne conserve pas de connexion permanente avec le proxy. Windows Media Services 9 Series dans Microsoft Windows Server 2003 prend en charge l’authentification NTLM via un serveur proxy, à condition que le proxy prenne en charge les connexions persistantes.

     

Comme indiqué, dans certains cas, l’application doit fournir les informations d’identification de l’utilisateur. Cela se produit par le biais de l’interface **IWMCredentialCallback** , qui a une méthode unique, **AcquireCredentials**. Pour prendre en charge l’authentification, implémentez cette interface dans votre application. L’objet lecteur interroge cette interface en appelant **QueryInterface** sur le pointeur [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) qu’il a reçu de l’application dans la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) . Si l’objet lecteur doit recevoir les informations d’identification de l’utilisateur, il appelle la méthode **AcquireCredentials** de l’application.

Si les informations d’identification sont envoyées sur le réseau sans chiffrement, le lecteur définit l' \_ \_ \_ indicateur de texte en clair des informations d’identification WMT dans le paramètre *pdwFlags* . Cela donne à l’application la possibilité d’avertir l’utilisateur que ses informations d’identification seront envoyées en texte brut.

Dans le cas contraire, l’objet lecteur chiffre automatiquement les informations d’identification avant de les envoyer sur le réseau. L’application peut les retourner à l’objet lecteur en texte brut. En outre, si l’objet lecteur définit l' \_ indicateur de chiffrement des informations d’identification WMT \_ , le lecteur prend en charge l’obtention d’informations d’identification chiffrées à partir de l’application. Dans ce cas, l’application peut soit retourner les informations d’identification en texte brut, soit les chiffrer elle-même à l’aide de la fonction **CryptProtectData** , qui est décrite dans la documentation du kit de développement logiciel (SDK) Platform. Si l’application chiffre les informations d’identification, elle doit définir l' \_ \_ indicateur de chiffrement des informations d’identification WMT dans le paramètre *pdwFlags* avant le retour de la méthode.

En règle générale, il n’est pas nécessaire de chiffrer les données, car l’objet lecteur chiffre les données si nécessaire. Toutefois, le chiffrement peut être utile si l’application conserve le nom d’utilisateur et le mot de passe en mémoire, car elle empêche une personne malveillante d’inspecter une image mémoire du processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




