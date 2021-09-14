---
title: Création d’un exemple de Project
description: Création d’un exemple de Project
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Lecteur Windows Media des magasins en ligne, création d’exemples de projets
- magasins en ligne, créer des exemples de projets
- type 2 magasins en ligne, création d’exemples de projets
- Lecteur Windows Media des magasins en ligne, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- Lecteur Windows Media les magasins en ligne, assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- plug-ins, Assistant projet
- plug-ins Lecteur Windows Media, assistant projet
- création d’exemples de projets
- exemples, type 2 magasins en ligne
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919312"
---
# <a name="creating-a-sample-project"></a>Création d’un exemple de Project

Pour créer un projet à l’aide de l’Assistant projet, procédez comme suit :

1.  Ouvrez Microsoft Visual Studio.
2.  Dans le menu **Fichier**, pointez sur **Nouveau**, puis cliquez sur **Projet**.
3.  dans la zone de liste **Types de Project** , choisissez **Visual C++ projets**.
4.  dans la zone de liste **modèles** , choisissez **Lecteur Windows Media assistant magasins en ligne**.
5.  Tapez un nom et un emplacement pour votre projet.
6.  Cliquez sur **OK** pour démarrer l’Assistant projet.
7.  Sélectionnez **type 2 (intégration de base)**, puis cliquez sur **suivant**.
8.  Tapez le nom convivial et l’ID du serveur de distribution de contenu pour votre service. Tapez l’URL de la page Web qui supprime le service de l’ordinateur de l’utilisateur.
    > [!Note]  
    > La valeur que vous fournissez pour l’ID de serveur de distribution de contenu ne doit pas contenir d’espaces. L’Assistant supprime tous les espaces de la chaîne que vous fournissez.

     

9.  Cliquez sur **Terminer** pour créer le projet.

L’Assistant génère automatiquement un nouveau projet C++ qui crée un plug-in de magasin en ligne de type 2 qui implémente les interfaces **IWMPSubscriptionService** et **IWMPSubscriptionService2** . Chaque fois que vous exécutez l’Assistant, il crée le même projet, mais le composant qui est créé lorsque vous compilez le projet a un ID de classe unique. Le nom du projet, le nom convivial et l’ID du serveur de distribution de contenu peuvent également être différents en fonction des valeurs que vous avez fournies lors de l’exécution de l’Assistant. L’exemple de projet inscrit le composant à l’aide d’un nom de clé qui correspond à la valeur que vous avez fournie pour le nom convivial.

L’exemple utilise du code Active Template Library (ATL) pour fournir des implémentations COM.

L’Assistant crée les fichiers suivants pour vous :

-   *NomProjet* dll. cpp. Implémente les exportations de la bibliothèque de liens dynamiques (DLL), telles que la fonction de point d’entrée DLL principale. Contient également le mappage d’objet ATL et la déclaration de module.
-   *NomProjet*. cpp. Contient des implémentations par défaut pour les méthodes des interfaces IWMPSubscriptionService et IWMPSubscriptionService2. contient également le code permettant de définir les boîtes de dialogue que l’exemple ouvre lorsque les méthodes sont appelées par Lecteur Windows Media.
-   *NomProjet*. def. Déclare les exportations de DLL.
-   StdAfx. cpp. Comprend des en-têtes standard.
-   WMP. h. fichier d’en-tête Lecteur Windows Media.
-   wmpplug. h. fichier d’en-tête du plug-in Lecteur Windows Media.
-   subscriptionservices. h. fichier d’en-tête des magasins en ligne Lecteur Windows Media.
-   Resource. h. Contient les définitions de ressource.
-   **NomProjet**. h. Contient les définitions de classe pour l’objet de magasin en ligne et les boîtes de dialogue. Définit l’ID de classe de l’objet et la constante d’ID du serveur de distribution de contenu.
-   StdAfx. h. Contient les inclusions système standard.
-   *NomProjet*. rc. Fichier de script de ressources. Contient des définitions pour les ressources et les contrôles de boîte de dialogue. Il s’agit également de l’emplacement de stockage de la table de chaînes. La table de chaînes contient vos constantes de chaîne de nom de projet et de nom convivial. en général, vous travaillez avec ce fichier dans le Visual Studio éditeur de ressources, et non en texte brut.
-   *NomProjet*. RGS. Fichier de script du Registre. ce fichier contient les informations utilisées pour ajouter votre classe de composant au registre afin que Lecteur Windows Media puisse la localiser. Vous pouvez modifier le nom de clé de votre service dans ce fichier.

> [!Note]  
> vous devez définir l’adresse de base de votre DLL sur 0x0F100000 pour éviter les conflits avec Lecteur Windows Media.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du plug-in pour un magasin de type 2 en ligne**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Interface IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interface IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




