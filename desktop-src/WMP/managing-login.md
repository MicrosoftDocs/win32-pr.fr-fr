---
title: Gestion de la connexion
description: Gestion de la connexion
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Online stores, gestion des connexions
- magasins en ligne, gestion des connexions
- tapez 1 magasins en ligne, gestion des connexions
- Windows Media Player Online stores, connexions
- magasins en ligne, connexions
- tapez 1 magasins en ligne, connexions
- Windows Media Player Online stores, processus de connexion standard
- magasins en ligne, processus de connexion standard
- types 1 magasins en ligne, processus de connexion standard
- Magasins en ligne du lecteur Windows Media, processus de déconnexion
- magasins en ligne, processus de déconnexion
- type 1 magasins en ligne, processus de déconnexion
- processus de connexion standard
- processus de déconnexion
- connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381521"
---
# <a name="managing-login"></a>Gestion de la connexion

Le lecteur Windows Media prend en charge différentes méthodes permettant à l’utilisateur de se connecter à un magasin de type 1 en ligne. Le lecteur fournit une boîte de dialogue de connexion standard, mais le magasin en ligne peut fournir une page Web qui constitue une alternative à la boîte de dialogue standard.

L’utilisateur peut lancer une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte fournie par le magasin en ligne. Si l’utilisateur initie une tentative de connexion en interagissant avec une page de découverte, le script sur la page de découverte appelle la méthode [External. attemptLogin](external-attemptlogin.md) .

L’état de connexion de l’utilisateur est géré par le magasin en ligne. Lorsque l’état de connexion de l’utilisateur change, ou si une tentative de connexion échoue, le plug-in du magasin en ligne avertit le lecteur Windows Media en appelant [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnLoginStateChange dans le paramètre de *type* . Le joueur transmet la notification en même temps que la page de découverte en déclenchant l’événement [External. OnLoginChange](external-onloginchange-event.md) .

Un appel à **OnLoginChange** ne signifie pas nécessairement que l’état de connexion de l’utilisateur a changé ; Cela peut signifier qu’une tentative de connexion a échoué. Pour déterminer l’état de connexion de l’utilisateur, le gestionnaire d’événements **OnLoginChange** peut inspecter la propriété [External. userLoggedIn](external-userloggedin.md) .

Les sections suivantes décrivent le processus de connexion standard, le processus de connexion alternatif et le processus de déconnexion.

## <a name="standard-log-in"></a>Connexion standard

Le processus de connexion standard implique les étapes suivantes :

1.  L’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Le lecteur Windows Media affiche une boîte de dialogue qui invite l’utilisateur à entrer un nom d’utilisateur et un mot de passe.
3.  Quand l’utilisateur clique sur le bouton **se connecter** dans la boîte de dialogue, le lecteur Windows Media appelle [IWMPContentPartner :: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), qui est implémenté par le plug-in du magasin en ligne.
4.  Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.
5.  Si la tentative de connexion réussit, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant true dans le membre **boolVal** du paramètre *pContext* . Si la tentative de connexion échoue, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant une valeur 32 bits dans le membre **UlVal** du paramètre *pContext* . Le lecteur transmet ensuite cette valeur 32 bits à [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) pour obtenir l’URL d’une page Web qui peut gérer l’échec.

## <a name="alternative-login"></a>Autre connexion

Si l’indicateur ALTLOGIN de l’abonnement \_ \_ est défini dans l’entrée de Registre **Capabilities** pour le plug-in du magasin en ligne, le lecteur Windows Media n’utilise pas la boîte de dialogue de connexion standard. Au lieu de cela, le lecteur Windows Media appelle **IWMPContentPartner :: GetItemInfo** pour récupérer l’URL d’une page Web qui exécute le processus de connexion. Pour plus d’informations sur l’entrée de Registre **Capabilities** , consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).

Le lecteur appelle **GetItemInfo** deux fois : après avoir passé g \_ szItemInfo \_ ALTLOGINURL pour récupérer l’URL de la page Web de connexion et après avoir passé g \_ szItemInfo \_ ALTLoginCaption pour récupérer la légende de la fenêtre qui héberge la page Web. Quand **GetItemInfo** retourne l’URL de la page Web de connexion, il peut spécifier la taille de la fenêtre de connexion en ajoutant la chaîne de paramètre suivante à l’URL :

? DlgX =*width*&DlgY =*hauteur*

Dans la chaîne de paramètre, la *largeur* et la *hauteur* sont la largeur et la hauteur de la fenêtre en pixels. Par exemple, **GetItemInfo** peut retourner la chaîne suivante pour spécifier que AltLogin.htm doit être affiché dans une fenêtre qui a une largeur de 800 pixels et une hauteur de 400 pixels


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Le processus de connexion alternatif implique les étapes suivantes :

1.  L’utilisateur initie une tentative de connexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Le lecteur Windows Media ouvre une fenêtre modale qui affiche la page Web de connexion fournie par le magasin en ligne.
3.  La page Web communique avec le magasin en ligne et réussit ou ne parvient pas à se connecter à l’utilisateur.
4.  Si la tentative de connexion aboutit, la page Web avertit le plug-in du magasin en ligne en appelant [External. SendMessage](external-sendmessage.md), ce qui entraîne un appel à [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). Le plug-in du magasin en ligne détermine que la tentative de connexion a réussi en examinant les paramètres passés à **IWMPContentPartner :: SendMessage**. Ces paramètres ne sont pas interprétés par le lecteur Windows Media ; ils n’ont de sens que dans le magasin en ligne. Le plug-in appelle **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant true dans le membre **boolVal** du paramètre *pContext* . Si la connexion échoue, le magasin en ligne doit déterminer comment aider l’utilisateur. L’une des possibilités consiste à afficher une nouvelle page Web dans la fenêtre modale qui héberge l’autre page de connexion.

## <a name="log-out"></a>Déconnectez-vous.

Le processus de déconnexion implique les étapes suivantes.

1.  L’utilisateur lance une tentative de déconnexion en interagissant avec l’interface utilisateur du lecteur Windows Media ou en interagissant avec une page de découverte.
2.  Le lecteur Windows Media appelle [IWMPContentPartner :: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), qui est implémenté par le plug-in du magasin en ligne.
3.  Le plug-in communique avec le magasin en ligne et réussit ou ne parvient pas à déconnecter l’utilisateur.
4.  Si la tentative de déconnexion réussit, le plug-in avertit le lecteur Windows Media en appelant **IWMPContentPartnerCallback :: Notify**, en passant \_ la valeur variant false dans le membre **boolVal** du paramètre *pContext* .

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

 

 




