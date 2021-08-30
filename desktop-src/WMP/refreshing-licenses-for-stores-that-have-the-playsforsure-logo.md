---
title: Actualisation des licences des magasins qui ont le logo PlaysForSure
description: Actualisation des licences des magasins qui ont le logo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Lecteur Windows Media des magasins en ligne, actualisation des licences
- magasins en ligne, actualisation des licences
- Lecteur Windows Media des magasins en ligne, actualisation des licences
- magasins en ligne, actualisation des licences
- Lecteur Windows Media les magasins en ligne, le logo PlaysForSure
- magasins en ligne, logo PlaysForSure
- actualisation des licences
- licences, actualisation
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3f59e7bfeb51af8c5c34d28d9819dc4eb4e29f2918b8a28c6e05e69f47d567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002799"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Actualisation des licences des magasins qui ont le logo PlaysForSure

certains magasins de musique en ligne ont le logo PlaysForSure mais ne sont pas intégrés à Lecteur Windows Media 11. ces magasins doivent fournir un document ServiceInfo et un composant léger afin que Lecteur Windows Media 11 puisse obtenir et mettre à jour des licences pour leur contenu.

L’exemple suivant illustre le fonctionnement du processus de mise à jour de la licence.

1.  L’utilisateur obtient des pistes de musique 50 à partir du magasin en ligne proseware. Chaque piste est un fichier avec l’extension de nom de fichier. WMA. Avec les pistes, l’utilisateur obtient des licences pour lire les pistes.
2.  l’utilisateur copie les pistes 50 sur un nouvel ordinateur sur lequel Lecteur Windows Media 11 est installé et ajoute les pistes à la bibliothèque Lecteur Windows Media.
3.  plus tard, le Module d’actualisation des licences (LRM), qui fait partie de Lecteur Windows Media 11, inspecte les métadonnées dans les pistes 50 et détermine que proseware est le fournisseur de contenu.
    > [!Note]  
    > Lecteur Windows Media est en mesure d’identifier le fournisseur de contenu en inspectant l’attribut **ContentDistributor** dans un fichier multimédia. si un magasin en ligne contenant le logo PlaysForSure fournit un fichier multimédia qui utilise Windows media Digital Rights Management (WMDRM), le magasin en ligne doit placer l’attribut **ContentDistributor** dans le fichier multimédia. pour plus d’informations, consultez ajout de l’attribut Content Distributor dans le kit de développement logiciel (SDK) Lecteur Windows Media.

     

4.  LRM recherche l’URL du document ServiceInfo de Proseware, télécharge le document et inspecte l’élément d' **installation** du document afin d’obtenir l’URL d’un package que le LRM peut utiliser pour installer le composant de proseware. Le LRM installe et charge le composant.
5.  Pour chacune des pistes 50, LRM appelle la méthode [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) du composant proseware. La méthode **allowPlay** place une licence pour la piste individuelle sur le nouvel ordinateur et retourne la **valeur true** dans le paramètre *pfAllowPlay* .
    > [!Note]  
    > Le composant Proseware doit fournir toutes les licences requises pour lire la piste individuelle. Autrement dit, le composant doit fournir une licence racine et une licence feuille si nécessaire.

     

    Lors du premier appel à la méthode **allowPlay** , le composant Proseware doit afficher une boîte de dialogue pour vérifier que l’utilisateur actuel possède un compte Proseware et a le droit de lire la piste. Lors des appels suivants à **allowPlay**, le composant peut utiliser les informations d’identification qu’il a obtenues dans le premier appel pour vérifier que l’utilisateur a le droit de lire les pistes restantes.

Le composant, qui est écrit par le magasin en ligne, doit implémenter la méthode **allowPlay** de l’interface **IWMPSubscriptionService** . Le composant doit retourner E \_ NOTIMPL à partir de chacune des trois autres méthodes : **allowCDBurn**, **allowPDATransfer** et **startBackgroundProcessing**. En outre, le composant doit définir la valeur de l’entrée de Registre **Capabilities** sur 1 ; autrement dit, l’indicateur de capacité ALLOWPLAY de l’abonnement \_ Cap \_ doit être défini, et tous les autres indicateurs de capacité doivent être effacés. Pour plus d’informations sur l’inscription du composant, consultez [clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).

Pour plus d’informations sur la création d’un composant qui implémente l’interface **IWMPSubscriptionService** , consultez [génération du plug-in pour un magasin de type 2 en ligne](building-the-plug-in-for-a-type-2-online-store.md).

pour plus d’informations sur la façon de fournir un document ServiceInfo à Microsoft, envoyez un e-mail à l’équipe des Services virtuels Lecteur Windows Media. L’adresse de messagerie de l’équipe est mpsvctm@microsoft.com .

pour obtenir des conseils techniques sur l’utilisation d’un large éventail de kits de développement logiciel (sdk) Windows pour créer un service proposant du contenu multimédia numérique sous licence, accédez au [centre de développement multimédia Microsoft Windows](https://msdn.microsoft.com/windowsmedia/default.aspx) et recherchez « création d’un magasin en ligne d’abonnement Lecteur Windows Media 10 ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Lecteur Windows Media Magasins en ligne**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




