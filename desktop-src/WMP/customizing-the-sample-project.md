---
title: Personnalisation de l’exemple de Project
description: Personnalisation de l’exemple de Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Lecteur Windows Media des magasins en ligne, personnalisation d’exemples de projets
- magasins en ligne, personnalisation des exemples de projets
- types 2 magasins en ligne, personnalisation des exemples de projets
- Lecteur Windows Media des magasins en ligne, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- personnalisation des exemples de projets
- exemples, type 2 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e83d6384529ea9b67c5132ec9cc1846da5e438
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881804"
---
# <a name="customizing-the-sample-project"></a>Personnalisation de l’exemple de Project

Lorsque vous créez votre propre magasin en ligne, vous pouvez modifier les implémentations des méthodes suivantes dans le fichier nommé YourProject. cpp :

-   **CYourProject :: allowPlay**. Utilisez cette fonction pour appliquer vos règles d’entreprise afin d’autoriser la lecture du contenu protégé.
-   **CYourProject :: allow cdburn**. Utilisez cette fonction pour appliquer vos règles d’entreprise pour permettre aux utilisateurs de copier du contenu protégé sur un CD.
-   **CYourProject :: allowPDATransfer**. Utilisez cette fonction pour appliquer vos règles d’entreprise pour permettre aux utilisateurs de transférer du contenu protégé vers un appareil mobile.
-   **CYourProject :: startBackgroundProcessing**. Utilisez cette fonction pour lancer les tâches de traitement en arrière-plan dont vous avez besoin. Par exemple, vous pouvez l’utiliser comme opportunité de vérifier les licences expirées.
-   **CYourProject ::D eviceavailable**. Utilisez cette fonction pour lancer des tâches liées à un appareil connecté.
-   **CYourProject ::P repareforsync**. Utilisez cette fonction pour effectuer les tâches nécessaires juste avant de synchroniser des médias numériques sur l’appareil.
-   **CYourProject :: serviceEvent**. Utilisez cette fonction pour commencer et terminer les tâches que vous souhaitez exécuter lorsque votre magasin en ligne est le magasin actif.
-   **CYourProject :: stopBackgroundProcessing**. utilisez cette fonction pour arrêter les tâches de traitement en arrière-plan que vous avez démarrées quand Lecteur Windows Media appelée **CYourProject :: startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Utilisation d’objets multimédias et playlists

La méthode **allowPlay** fournit un pointeur vers l’interface **IWMPMedia** en tant que paramètre. cette interface est l’interface Lecteur Windows Media qui représente les objets multimédias. En appelant les méthodes sur cette interface, vous pouvez utiliser les attributs et les propriétés d’un élément multimédia individuel.

Les méthodes **allowCDBurn** et **allowPDATransfer** fournissent un pointeur vers l’interface **IWMPPlaylist** en tant que paramètre. cette interface est l’interface Lecteur Windows Media qui représente les objets de sélection. En appelant les méthodes sur cette interface, vous pouvez utiliser les attributs et les propriétés d’une sélection, ajouter des éléments à une sélection ou supprimer des éléments d’une sélection.

Pour savoir comment supprimer un élément d’une sélection par programme, consultez l’implémentation de **CAllowBaseDialog &lt; T &gt; :: OnRemoveMediaFromPlaylist**. Pour en savoir plus sur l’utilisation des objets multimédias et playlist, consultez [modèle objet Player pour les langages de script](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Code pouvant être supprimé

Vous souhaiterez probablement supprimer le code qui ouvre les boîtes de dialogue, car il est peu probable que vous souhaitiez que les utilisateurs décident des éléments multimédias qui peuvent être lus ou copiés. À partir de YourProject. h, supprimez le code suivant :

-   Déclaration de **CAllowBaseDialog**.
-   Déclaration de **CAllowBurnDialog**.
-   Déclaration de **CAllowTransferDialog**.

À partir de YourProject. cpp, supprimez le code suivant :

-   Implémentation de **CAllowBaseDialog &lt; T &gt; :: OnInitDialog**.
-   Implémentation de **CAllowBaseDialog &lt; T &gt; :: OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du plug-in pour un magasin de type 2 en ligne**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




