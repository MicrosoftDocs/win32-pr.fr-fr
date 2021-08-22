---
title: Gestion de la connexion
description: Gestion de la connexion
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Lecteur Windows Media des magasins en ligne, gestion des connexions
- magasins en ligne, gestion des connexions
- tapez 1 magasins en ligne, gestion des connexions
- Lecteur Windows Media des magasins en ligne, connexions
- magasins en ligne, connexions
- tapez 1 magasins en ligne, connexions
- Lecteur Windows Media les magasins en ligne, processus de connexion standard
- magasins en ligne, processus de connexion standard
- types 1 magasins en ligne, processus de connexion standard
- Lecteur Windows Media les magasins en ligne, processus de déconnexion
- magasins en ligne, processus de déconnexion
- type 1 magasins en ligne, processus de déconnexion
- processus de connexion standard
- processus de déconnexion
- connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698385f2d5a618899bd4fe440db5a552859c7647ceb2ae11e02b773c96479d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135172"
---
# <a name="managing-login"></a>Gestion de la connexion

Lecteur Windows Media prend en charge diverses méthodes permettant à l’utilisateur de se connecter à un magasin de type 1 en ligne. Le lecteur fournit une boîte de dialogue de connexion standard, mais le magasin en ligne peut fournir une page Web qui constitue une alternative à la boîte de dialogue standard.

l’utilisateur peut lancer une tentative de connexion en interagissant avec l’interface utilisateur Lecteur Windows Media ou en interagissant avec une page de découverte fournie par le magasin en ligne. Si l’utilisateur initie une tentative de connexion en interagissant avec une page de découverte, le script sur la page de découverte appelle la méthode [External. attemptLogin](external-attemptlogin.md) .

L’état de connexion de l’utilisateur est géré par le magasin en ligne. lorsque l’état de connexion de l’utilisateur change, ou si une tentative de connexion échoue, le plug-in du magasin en ligne notifie Lecteur Windows Media en appelant [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnLoginStateChange dans le paramètre de *type* . Le joueur transmet la notification en même temps que la page de découverte en déclenchant l’événement [External. OnLoginChange](external-onloginchange-event.md) .

Un appel à **OnLoginChange** ne signifie pas nécessairement que l’état de connexion de l’utilisateur a changé ; Cela peut signifier qu’une tentative de connexion a échoué. Pour déterminer l’état de connexion de l’utilisateur, le gestionnaire d’événements **OnLoginChange** peut inspecter la propriété [External. userLoggedIn](external-userloggedin.md) .

Les sections suivantes décrivent le processus de connexion standard, le processus de connexion alternatif et le processus de déconnexion.

## <a name="standard-log-in"></a>Connexion standard

Le processus de connexion standard implique les étapes suivantes :

1.  l’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur Lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Lecteur Windows Media affiche une boîte de dialogue qui invite l’utilisateur à entrer un nom d’utilisateur et un mot de passe.
3.  quand l’utilisateur clique sur le bouton **se connecter** dans la boîte de dialogue, Lecteur Windows Media appelle [IWMPContentPartner :: Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), qui est implémenté par le plug-in du magasin en ligne.
4.  Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.
5.  si la tentative de connexion réussit, le plug-in notifie Lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur VARIANT TRUE dans le membre **boolVal** du paramètre *pContext* . si la tentative de connexion échoue, le plug-in notifie Lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant une valeur 32 bits dans le membre **ulVal** du paramètre *pContext* . Le lecteur transmet ensuite cette valeur 32 bits à [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) pour obtenir l’URL d’une page Web qui peut gérer l’échec.

## <a name="alternative-login"></a>Autre connexion

si l’indicateur ALTLOGIN de l’abonnement \_ \_ est défini dans l’entrée de registre **Capabilities** pour le plug-in du magasin en ligne, Lecteur Windows Media n’utilise pas la boîte de dialogue de connexion standard. au lieu de cela, Lecteur Windows Media appelle **IWMPContentPartner :: GetItemInfo** pour récupérer l’URL d’une page web qui exécute le processus de connexion. Pour plus d’informations sur l’entrée de Registre **Capabilities** , consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).

Le lecteur appelle **GetItemInfo** deux fois : après avoir passé g \_ szItemInfo \_ ALTLOGINURL pour récupérer l’URL de la page Web de connexion et après avoir passé g \_ szItemInfo \_ ALTLoginCaption pour récupérer la légende de la fenêtre qui héberge la page Web. Quand **GetItemInfo** retourne l’URL de la page Web de connexion, il peut spécifier la taille de la fenêtre de connexion en ajoutant la chaîne de paramètre suivante à l’URL :

? DlgX =*width*&DlgY =*hauteur*

Dans la chaîne de paramètre, la *largeur* et la *hauteur* sont la largeur et la hauteur de la fenêtre en pixels. Par exemple, **GetItemInfo** peut retourner la chaîne suivante pour spécifier que AltLogin.htm doit être affiché dans une fenêtre qui a une largeur de 800 pixels et une hauteur de 400 pixels


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Le processus de connexion alternatif implique les étapes suivantes :

1.  l’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur Lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Lecteur Windows Media ouvre une fenêtre modale qui affiche la page web de connexion fournie par le magasin en ligne.
3.  La page Web communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.
4.  Si la tentative de connexion aboutit, la page Web avertit le plug-in du magasin en ligne en appelant [External. SendMessage](external-sendmessage.md), ce qui entraîne un appel à [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). Le plug-in du magasin en ligne détermine que la tentative de connexion a réussi en examinant les paramètres passés à **IWMPContentPartner :: SendMessage**. ces paramètres ne sont pas interprétés par Lecteur Windows Media ; ils n’ont de sens que dans le magasin en ligne. Le plug-in appelle **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant true dans le membre **boolVal** du paramètre *pContext* . Si la connexion échoue, le magasin en ligne doit déterminer comment aider l’utilisateur. L’une des possibilités consiste à afficher une nouvelle page Web dans la fenêtre modale qui héberge l’autre page de connexion.

## <a name="log-out"></a>Déconnectez-vous.

Le processus de déconnexion implique les étapes suivantes.

1.  l’utilisateur lance une tentative de déconnexion en interagissant avec l’interface utilisateur Lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Lecteur Windows Media appelle [IWMPContentPartner :: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), qui est implémenté par le plug-in du magasin en ligne.
3.  Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à déconnecter l’utilisateur.
4.  si la tentative de déconnexion réussit, le plug-in notifie Lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur VARIANT false dans le membre **boolVal** du paramètre *pContext* .

En cas de réussite d’une tentative de connexion ou d’extraction, le plug-in du magasin en ligne appelle **IWMPContentPartnerCallback :: Notify**, en passant wmpcnLoginStateChange dans le paramètre de *type* . Le plug-in utilise le paramètre *pContext* pour spécifier l’état actuel de la connexion de l’utilisateur. Si le plug-in affecte à *pContext* -> **boolVal** la \_ valeur true, l’utilisateur est connecté. Si le plug-in affecte à *pContext* -> **boolVal** la \_ valeur false, l’utilisateur se déconnecte. Notez que *pContext* n’indique pas la réussite ou l’échec de la tentative ; au lieu de cela, il indique l’état de connexion actuel de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. OnLoginChange, événement**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner :: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner :: Logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




