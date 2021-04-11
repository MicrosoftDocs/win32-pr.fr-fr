---
title: Actualisation des licences des magasins qui ont le logo PlaysForSure
description: Actualisation des licences des magasins qui ont le logo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online stores, actualisation des licences
- magasins en ligne, actualisation des licences
- Windows Media Player Online stores, actualisation des licences
- magasins en ligne, actualisation des licences
- Windows Media Player Online stores, logo PlaysForSure
- magasins en ligne, logo PlaysForSure
- actualisation des licences
- licences, actualisation
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101289"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Actualisation des licences des magasins qui ont le logo PlaysForSure

Certains magasins de musique en ligne ont le logo PlaysForSure mais ne sont pas intégrés au lecteur Windows Media 11. Ces magasins doivent fournir un document ServiceInfo et un composant léger afin que le lecteur Windows Media 11 puisse obtenir et mettre à jour des licences pour son contenu.

L’exemple suivant illustre le fonctionnement du processus de mise à jour de la licence.

1.  L’utilisateur obtient des pistes de musique 50 à partir du magasin en ligne proseware. Chaque piste est un fichier avec l’extension de nom de fichier. WMA. Avec les pistes, l’utilisateur obtient des licences pour lire les pistes.
2.  L’utilisateur copie les pistes 50 sur un nouvel ordinateur sur lequel est installé le lecteur Windows Media 11 et ajoute les pistes à la bibliothèque du lecteur Windows Media.
3.  Plus tard, le module d’actualisation des licences (LRM), qui fait partie du lecteur Windows Media 11, inspecte les métadonnées dans les pistes 50 et détermine que Proseware est le fournisseur de contenu.
    > [!Note]  
    > Le lecteur Windows Media est en mesure d’identifier le fournisseur de contenu en inspectant l’attribut **ContentDistributor** dans un fichier multimédia. Si un magasin en ligne contenant le logo PlaysForSure fournit un fichier multimédia qui utilise Windows Media Digital Rights Management (WMDRM), le magasin en ligne doit placer l’attribut **ContentDistributor** dans le fichier multimédia. Pour plus d’informations, consultez Ajout de l’attribut content Distributor dans le kit de développement logiciel (SDK) du lecteur Windows Media.

     

4.  LRM recherche l’URL du document ServiceInfo de Proseware, télécharge le document et inspecte l’élément d' **installation** du document afin d’obtenir l’URL d’un package que le LRM peut utiliser pour installer le composant de proseware. Le LRM installe et charge le composant.
5.  Pour chacune des pistes 50, LRM appelle la méthode [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) du composant proseware. La méthode **allowPlay** place une licence pour la piste individuelle sur le nouvel ordinateur et retourne la **valeur true** dans le paramètre *pfAllowPlay* .
    > [!Note]  
    > Le composant Proseware doit fournir toutes les licences requises pour lire la piste individuelle. Autrement dit, le composant doit fournir une licence racine et une licence feuille si nécessaire.

     

    Lors du premier appel à la méthode **allowPlay** , le composant Proseware doit afficher une boîte de dialogue pour vérifier que l’utilisateur actuel possède un compte Proseware et a le droit de lire la piste. Lors des appels suivants à **allowPlay**, le composant peut utiliser les informations d’identification qu’il a obtenues dans le premier appel pour vérifier que l’utilisateur a le droit de lire les pistes restantes.

Le composant, qui est écrit par le magasin en ligne, doit implémenter la méthode **allowPlay** de l’interface **IWMPSubscriptionService** . Le composant doit retourner E \_ NOTIMPL à partir de chacune des trois autres méthodes : **allowCDBurn**, **allowPDATransfer** et **startBackgroundProcessing**. En outre, le composant doit définir la valeur de l’entrée de Registre **Capabilities** sur 1 ; autrement dit, l’indicateur de capacité ALLOWPLAY de l’abonnement \_ Cap \_ doit être défini, et tous les autres indicateurs de capacité doivent être effacés. Pour plus d’informations sur l’inscription du composant, consultez [clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).

Pour plus d’informations sur la création d’un composant qui implémente l’interface **IWMPSubscriptionService** , consultez [génération du plug-in pour un magasin de type 2 en ligne](building-the-plug-in-for-a-type-2-online-store.md).

Pour plus d’informations sur la façon de fournir un document ServiceInfo à Microsoft, envoyez un e-mail à l’équipe des services virtuels du lecteur Windows Media. L’adresse de messagerie de l’équipe est mpsvctm@microsoft.com .

Pour obtenir des conseils techniques sur l’utilisation de divers kits de développement logiciel (SDK) Windows Media pour créer un service proposant du contenu multimédia numérique sous licence, accédez au [Centre de développement Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) et recherchez « création d’un magasin en ligne d’abonnement Windows Media Player 10 ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Windows Media Player Online stores**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




