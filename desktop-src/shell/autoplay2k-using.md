---
description: Lorsque l’interpréteur de commandes détecte l’insertion d’un nouveau média ou la pièce jointe d’un périphérique enfichable à chaud, le contenu du périphérique ou du support est déterminé. La lecture automatique, en fonction de ses paramètres actuels, effectue l’une des opérations suivantes.
title: Utilisation et configuration de l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 35de48ee77cde7c598088b3f3877083efc2151f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296127"
---
# <a name="using-and-configuring-autoplay"></a>Utilisation et configuration de l’exécution automatique

Lorsque l’interpréteur de commandes détecte l’insertion d’un nouveau média ou la pièce jointe d’un périphérique enfichable à chaud, le contenu du périphérique ou du support est déterminé. La lecture automatique, en fonction de ses paramètres actuels, effectue l’une des opérations suivantes.

-   Lit le contenu automatiquement.
-   Affiche une boîte de dialogue invitant l’utilisateur à choisir un gestionnaire par défaut pour un type de contenu unique.
-   Présente, dans le cas d’un contenu mixte, une liste d’applications de gestionnaire disponibles à lancer. Le gestionnaire choisi lit ensuite automatiquement son type de contenu associé.
-   Affiche un affichage des dossiers standard des fichiers.
-   Ne fait rien si, précédemment, l’utilisateur a choisi n' **effectuer aucune action** pour ce type de contenu, et spécifié **toujours effectuer l’action sélectionnée**.

si le contenu ne répond pas aux critères de lecture automatique, l’événement est ensuite transmis à Windows Acquisition d’images (WIA).

Les rubriques suivantes traitent de la configuration et de l’utilisation de la lecture automatique.

-   [Préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Comment la fonctionnalité d’exécution automatique recherche les médias](#how-autoplay-searches-media)
-   [Définition de types de contenu unique et mixte](#defining-single-and-mixed-content-types)
-   [Exemples de scénarios](#sample-scenarios)
    -   [lecture automatique pour Stockage appareils avec image multimédia](#autoplay-for-storage-devices-with-picture-media)
    -   [lecture automatique pour Musique les appareils de lecture de fichiers et les appareils Stockage contenant Musique média](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Lecture automatique pour la lecture vidéo lors de la première présentation](#autoplay-for-video-playback-on-first-presentation)
-   [Affectation d’applications de gestionnaire par défaut](#assigning-default-handler-applications)
-   [Gestion des médias contenant des types de contenu mixtes](#handling-media-containing-mixed-content-types)
-   [Interfaces utilisateur de lecture automatique](#autoplay-user-interfaces)
    -   [Type de contenu unique, boîte de dialogue](#single-content-type-dialog-box)
    -   [Boîte de dialogue mixte de média](#mixed-media-dialog-box)
    -   [Page Propriété](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Préparation du matériel et des logiciels à utiliser avec l’exécution automatique

Plusieurs informations doivent apparaître dans le registre pour que l’exécution automatique fonctionne. Ces informations interagissent et se référencent les unes aux autres pour former l’intégralité de l’environnement d’exécution automatique. Ce document présente la configuration de chacun de ces éléments d’information sous la forme d’une procédure autonome individuelle.

Pour obtenir des instructions supplémentaires, consultez les rubriques suivantes.

-   [Comment affecter un gestionnaire d’appareils à un appareil](how-to-assign-a-device-handler-to-a-device.md)
-   [Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Comment empêcher l’exécution automatique d’un composant](how-to-prevent-autoplay-for-a-component.md)
-   [Comment inscrire un gestionnaire pour un événement d’appareil](how-to-register-a-handler-for-a-device-event.md)
-   [Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution](how-to-use-autoplay-events-in-running-applications.md)
-   [Comment inscrire un gestionnaire d’événements](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Comment la fonctionnalité d’exécution automatique recherche les médias

L’exécution automatique recherche les quatre niveaux de répertoire du média sous le répertoire racine pour rechercher les types de fichiers connus. Elle utilise la valeur PerceivedType associée à une extension de nom de fichier dans le registre pour déterminer la catégorie de fichier, qu’il s’agisse d’une image, d’un fichier audio ou d’un fichier vidéo. Avec ces informations, l’exécution automatique lance le gestionnaire approprié pour l’appareil et le type de fichier. Pour plus d’informations, consultez [types perçus et inscription des applications](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Définition de types de contenu unique et mixte

L’exécution automatique définit trois catégories de contenu principales.

-   Images
-   Musique
-   Vidéo

Un support est considéré comme contenant un type de contenu unique si tous les fichiers sur le support appartiennent à une seule de ces trois catégories. Notez que cela ne signifie pas que les fichiers doivent être du même type de *fichier* ; .jpg, .gif et .bmp sont des types de fichiers différents, mais un type de contenu (images).

Si les types de contenu pris en charge sont présents sur le support, mais qu’aucun type de contenu ne peut prendre en compte 100% du total, le support est considéré comme contenant un type de contenu mixte et est géré en conséquence. Pour plus d’informations, consultez [gestion des médias contenant des types de contenu mixtes](#handling-media-containing-mixed-content-types).

## <a name="sample-scenarios"></a>Exemples de scénarios

Les scénarios suivants fournissent une compréhension élémentaire des éléments à attendre de l’exécution automatique.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>lecture automatique pour Stockage appareils avec image multimédia

1.  L’utilisateur attache un lecteur USB SanDisk CompactFlash qui a déjà un support inséré contenant le type de contenu d’image 100 pour cent sous la forme de fichiers .jpg.
2.  La notification affiche **le nouveau matériel-SanDisk ImageMate**.
3.  L’exécution automatique lance l’application d’image appropriée.

De même, lorsque l’utilisateur insère le même média CompactFlash dans le lecteur alors que le lecteur est déjà attaché au système, l’événement Media Insert fait également en sorte que l’exécution automatique lance l’application diaporama d’images. L’utilisateur a la possibilité d’accéder à la page des propriétés du périphérique multimédia SanDisk pour remplacer la valeur par défaut par une autre application d’exécution automatique inscrite, telle que l’Assistant scanneur et appareil photo, ou Picture It !.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>lecture automatique pour Musique les appareils de lecture de fichiers et les appareils Stockage contenant Musique média

1.  L’utilisateur attache un lecteur MP3 Diamond Rio USB.
2.  La notification affiche **un nouveau matériel-lecteur MP3 Diamond Rio**.
3.  l’exécution automatique lit les fichiers à l’aide de son gestionnaire par défaut enregistré, par exemple Lecteur Windows Media.

de même, si l’utilisateur insère un support contenant des fichiers .mp3 (par exemple, CompactFlash, SmartMedia, memory Stick ou CD-rom) qui compte 100% du contenu total pris en charge dans un dispositif de stockage, l’événement media insert entraîne également la lecture des fichiers par la lecture automatique à l’aide de la Lecteur Windows Media. L’utilisateur peut accéder à la feuille de propriétés du dispositif de stockage et remplacer l’action par défaut par une autre application de lecture automatique inscrite, telle que WinAmp ou Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Lecture automatique pour la lecture vidéo lors de la première présentation

1.  L’utilisateur se connecte à une caméra vidéo numérique 1394 pour la première fois.
2.  L’utilisateur reçoit une boîte de dialogue simple qui demande l’exécution de l’application. Les choix sont d’exécuter l’une des applications de lecture automatique inscrite ou d’ouvrir un dossier pour afficher les fichiers. L’utilisateur peut définir le comportement sélectionné pour qu’il soit enregistré en tant qu’action par défaut pour les événements de connexion à chaud d’une caméra vidéo numérique.

## <a name="assigning-default-handler-applications"></a>Affectation d’applications de gestionnaire par défaut

une nouvelle installation de Windows recherche l’exécution automatique avec un ensemble d’applications de gestionnaire inscrites. les Applications inscrites par défaut au cours d’une installation Windows sont les suivantes.




| Type de support | Applications | 
|------------|--------------|
| Images | <ul><li>Diaporama (par défaut)</li><li>Assistant appareil photo et scanneur</li><li>Assistant impression</li><li>Ouvrir le dossier</li></ul> | 
| Musique | <ul><li>Lecteur Windows Media (par défaut)</li><li>Ouvrir le dossier</li></ul> | 
| Vidéo | <ul><li>Lecteur Windows Media (par défaut)</li><li>Ouvrir le dossier</li></ul> | 




 

Dans le cas de types non pris en charge, les utilisateurs sont invités à attribuer le paramètre par défaut de l’action d’exécution automatique associée à chaque périphérique de stockage lors de sa première introduction au système. À ce moment-là, l’utilisateur est invité à choisir une action dans une liste fournie d’applications inscrites ou à afficher un affichage des dossiers qui répertorie le contenu du média. L’utilisateur a également la possibilité de choisir d’être invité à chaque fois que le type de média est détecté, plutôt que d’enregistrer une application particulière par défaut.

> [!Note]  
> Les fabricants de périphériques ont la possibilité d’inscrire et d’attribuer des applications par défaut à utiliser avec leurs produits spécifiques. Dans ce cas, la boîte de dialogue offrant un choix à l’utilisateur n’est pas affichée.

 

Pour être proposé en tant qu’option de gestionnaire par l’exécution automatique, les applications nouvellement installées doivent s’inscrire dans le registre. Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).

Les utilisateurs peuvent toujours modifier le gestionnaire d’exécution automatique par défaut pour n’importe quel périphérique de stockage ou type de contenu. La page de propriétés lecture automatique est accessible en modification dans la feuille de propriétés du dispositif de stockage dans **poste de travail**.

Pour obtenir des exemples d’invites utilisateur et de pages de propriétés, consultez [lecture automatique d’interfaces utilisateur](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Gestion des médias contenant des types de contenu mixtes

Lorsque l’exécution automatique est présentée avec un support de contenu mixte, elle nécessite une intervention de l’utilisateur avant de pouvoir agir. Dans ce cas, une boîte de dialogue contenant une liste filtrée de toutes les applications inscrites appropriées disponibles pour les types de contenu présents sur le média est présentée à l’utilisateur. L’utilisateur peut choisir l’une de ces applications pour effectuer une lecture automatique de ce type de contenu particulier, tandis que le reste reste intact. Étant donné que la composition d’un contenu mixte varie avec chaque disque, il n’existe aucune option permettant d’enregistrer ce choix par défaut.

Pour obtenir des exemples d’invites utilisateur, consultez [lecture automatique d’interfaces utilisateur](#autoplay-user-interfaces).

## <a name="autoplay-user-interfaces"></a>Interfaces utilisateur de lecture automatique

Il existe trois interfaces utilisateur possibles.

-   Boîte de dialogue qui invite l’utilisateur à entrer une action pour un type de contenu unique
-   Boîte de dialogue qui invite l’utilisateur à entrer une action pour les types de contenu mixtes
-   Une page de propriétés

### <a name="single-content-type-dialog-box"></a>Type de contenu unique, boîte de dialogue

Une boîte de dialogue similaire à ce qui suit s’affiche quand un support pris en charge n’a pas encore été affecté à une action d’exécution automatique par défaut est présenté au système.

![capture d’écran de la boîte de dialogue de type de contenu unique](images/pix.png)

Les utilisateurs peuvent effectuer l’une des opérations suivantes.

-   Choisissez une action dans la liste des applications inscrites.
-   Répertoriez les fichiers sur le support dans un affichage normal du dossier.
-   Aucune action n’est nécessaire.

Un utilisateur peut également enregistrer un choix en tant qu’action par défaut pour ce support en cliquant sur la zone **toujours faire l’action sélectionnée** . Une fois ce choix effectué, la boîte de dialogue ne s’affiche plus. toutefois, dans Windows XP Service Pack 1 (SP1), si une nouvelle application capable de gérer un type de média particulier est ajoutée à l’ordinateur, la boîte de dialogue est à nouveau présentée à l’utilisateur, ce qui lui donne la possibilité de sélectionner la nouvelle application comme action d’exécution par défaut. Les applications peuvent également se définir comme sélection par défaut lorsqu’elles sont installées.

Windows XP SP1 ajoute également une fonctionnalité qui conserve le choix de l’action d’exécution automatique de l’utilisateur s’il ne clique pas sur la zone **toujours faire l’action sélectionnée** . Si un utilisateur choisit une action d’exécution automatique pour une instance unique, la prochaine fois que cette boîte de dialogue est présentée pour ce type de média, la même action est la sélection par défaut.

Pour qu’une application soit incluse dans la liste des actions possibles, elle doit être inscrite avec l’exécution automatique. Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Boîte de dialogue mixte de média

La boîte de dialogue suivante s’affiche lorsqu’un support contenant un mélange de types de fichiers pris en charge est présenté au système. Il s’agit essentiellement de la même boîte de dialogue de support de contenu, mais avec deux différences significatives. Tout d’abord, les options d’action disponibles consistent en une liste filtrée d’applications pertinentes pour tous les types de contenu présents sur le support. Deuxièmement, il n’est pas possible de choisir une action par défaut permanente, car les types de contenu et les pourcentages de médias de contenu mixte sont trop imprévisibles.

![capture d’écran de la boîte de dialogue de média mixte](images/mix.png)

Pour qu’une application soit incluse dans la liste des actions possibles, elle doit être inscrite avec l’exécution automatique. Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Page Propriété

Voici un exemple de page de propriétés d’exécution automatique pour un périphérique DVD/CD-ROM.

![capture d’écran de la page de propriétés](images/apdlg.png)

Chaque type d’appareil offre un sous-ensemble approprié de types de contenu pour la configuration de l’exécution automatique. À son tour, chaque type de contenu, lorsqu’il est sélectionné, offre une liste appropriée des options d’action dans la zone de liste. Une action différente peut être choisie pour chaque type de contenu.

 

 



