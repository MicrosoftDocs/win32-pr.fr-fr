---
title: Structure de l’exemple d’application de bureau
description: Structure de l’exemple d’application de bureau
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemples, applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fb377c1bb6ebf943721b55ec6175e65f70ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673613"
---
# <a name="structure-of-the-sample-desktop-application"></a>Structure de l’exemple d’application de bureau

L’exemple d’application de bureau se compose de deux parties principales :

-   Le projet wmdapp contient la plupart des classes qui affichent l’interface utilisateur, gèrent le glisser-déplacer et effectuent toutes les fonctionnalités requises du programme.
-   Le projet proghelp est une application d’assistance qui contient des classes non essentielles pour gérer les notifications d’État et les transferts de fichiers manuels du bureau vers l’application.

L’exécutable utilise le projet d’assistance uniquement lorsque l’utilisateur sélectionne **utiliser l’interface** de l’opération dans le menu **options** pour gérer le transfert de fichiers manuel vers l’appareil et pour incrémenter la barre d’État dans le formulaire de progression du téléchargement. Tout le reste de l’application est géré dans le projet wmdapp.



| Classe                | Fichier                    | Description                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp. cpp             | Classe qui gère la fenêtre parente de l’interface utilisateur. Le code de ce fichier gère également une entrée utilisateur non gérée par CDevFiles, telle que la création d’une sélection ou d’un album sur un appareil, la suppression de fichiers et l’inscription de choix de menu.                                                                                                                                                    |
| CDevices             | Devices. cpp             | Classe qui gère le volet gauche de la fenêtre d’application principale, où les périphériques disponibles sont répertoriés. Cette classe gère la boucle de messagerie, qui gère les entrées d’utilisateur, telles que la sélection d’un appareil et la notification au volet CDevFiles de charger les fichiers appropriés lorsque la sélection de l’appareil a été modifiée.                                                                              |
| CDevFiles            | Devfiles. cpp            | Classe qui gère le volet de droite de la fenêtre d’application principale, où les fichiers sur l’appareil sélectionné sont répertoriés. Cette classe gère la boucle de messagerie et gère l’entrée de l’utilisateur, par exemple, en faisant glisser des fichiers sur l’appareil et en supprimant des fichiers de l’appareil.                                                                                                                          |
| CStatus              | État. cpp              | Classe qui gère la barre d’État inférieure dans la fenêtre principale, où le nombre de périphériques et de fichiers est indiqué, ainsi que la quantité de mémoire disponible et utilisée sur l’appareil sélectionné.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr. cpp            | Interface de niveau supérieur pour Windows Media Gestionnaire de périphériques. Cette classe gère l’authentification, récupère l’interface **IWMDeviceManager** de niveau supérieur et s’inscrit pour les notifications avec l’interface **IWMDMNotification** .                                                                                                                                                                  |
| CProgress            | Progress. cpp            | Classe dans le projet d’application principal qui crée et gère la boîte de dialogue indiquant la progression d’un événement.                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData. cpp            | Classe wrapper qui contient un pointeur vers un stockage (si représente un fichier ou un dossier sur l’appareil) ou un appareil (si représente un appareil), ainsi qu’une variété d’informations sur l’objet, notamment la taille et les attributs.                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler. cpp | Gère l’arrivée des appareils et les notifications de suppression en alertant la fenêtre CDevices.                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper. cpp      | Créé par CDevFiles dans les fonctions locales pour recevoir des notifications de Windows Media Gestionnaire de périphériques en implémentant **IWMDMProgress**. Elle est utilisée par la classe CProgress pour déterminer la quantité de barres dans la barre de progression et lorsqu’une action est terminée. Cette classe est définie comme un objet COM qui expose l’interface du kit de développement logiciel (SDK) **IWMDMProgress** et une interface personnalisée IWMDMProgressHelper. |
| COperationHelper     | Operationhelper. cpp     | Cette classe implémente **IWMDMOperation** pour gérer le transfert manuel de fichiers. Elle est multithread pour lui permettre de se produire de manière asynchrone et est définie comme un objet COM qui expose une interface personnalisée, IWMDMOperationHelper, pour instancier et initialiser la classe. Cette classe est utilisée uniquement si l’utilisateur sélectionne « utiliser l’interface de l’opération » dans le menu **options** .                            |



 

Les listes suivantes décrivent les étapes de base qui se produisent pour différentes actions de l’utilisateur :

**Au démarrage**

Les étapes principales suivantes se produisent lorsque l’exemple d’application est démarré.

1.  La variable CWMDM globale est instanciée et authentifiée et s’inscrit pour recevoir des notifications
2.  Un CDevices global est instancié et CDevices :: Create est appelé pour créer et remplir le volet périphériques.
3.  Un CDevFiles global est instancié et CDevFiles :: Create est appelé pour créer le volet fichiers (qui n’est pas rempli tant que l’utilisateur n’a pas sélectionné un appareil).
4.  Un CStatus global est instancié et CStatus :: Create est appelé pour instancier la barre d’État.
5.  \_OnViewRefresh énumère tous les appareils et initialise et ajoute tous les appareils (CItemData) à CDevices et met à jour la barre d’État pour afficher le nombre d’appareils.
6.  CDevices :: AddItem ajoute l’élément à l’arborescence qui représente les appareils, avec un pointeur vers lui-même en tant que TVITEM. lParam. Tous les objets CDevice (appareils) et CDevFiles (fichier) sont stockés dans ce membre du nœud TreeView dans la fenêtre appropriée.

**Sur la sélection d’un appareil**

Les étapes principales suivantes se produisent lorsque l’utilisateur sélectionne un appareil dans le volet gauche de la fenêtre d’application.

1.  La fenêtre CDevices intercepte un clic et envoie un \_ message WM DRM \_ UPDATEDEVICE à lui-même.
2.  CDevices reçoit son propre message et appelle UpdateSelection, qui indique à l’objet CDevFiles global de tout effacer, d’énumérer tous les éléments de niveau supérieur de l’appareil et appelle CDevFiles :: AddItem pour ajouter chaque élément au volet fichiers.
3.  Enfin, CDevices appelle CDevFiles :: UpdateStatusBar pour mettre à jour la barre d’État avec les informations de périphérique et de fichier appropriées.

**Création d’une sélection**

Après avoir cliqué sur « créer une sélection » dans le menu **conteneurs** , l’application appelle la fonction locale \_ OnCreatePlaylist, qui effectue les actions suivantes :

1.  Obtient le nombre d’éléments sélectionnés à partir de la variable globale CDevFiles.
2.  Appelez la fonction locale DlgNamePlaylist pour ouvrir une boîte de dialogue et obtenir un nom pour la sélection.
3.  Appelez CProgress :: Create pour créer une fenêtre de boîte de dialogue qui indique la progression de l’action, puis définissez les paramètres de la classe CProgress, tels que le texte du titre, la plage, la valeur actuelle, etc.
4.  Parcourez tous les éléments sélectionnés dans l’arborescence CDevFiles et demandez l’objet CItemData associé à chaque fichier sélectionné dans l’arborescence, en incrémentant la barre de la boîte de dialogue de progression avec chaque fichier. Les fichiers sont ajoutés à un tableau d’interfaces [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) .
5.  Obtient un handle vers l’élément actuellement sélectionné et l’interroger pour une interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) , qui sera utilisée ultérieurement pour créer la nouvelle sélection sur l’appareil.
6.  Interrogez l’objet sélectionné pour [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)et appelez [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) pour créer une nouvelle interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata).
7.  Ajoutez le \_ Code de format WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST à la nouvelle interface **IWMDMMetadata** et créez une sélection sur l’appareil en appelant [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3), en passant l’interface de métadonnées. La méthode récupère un pointeur vers le nouveau **IWMDMStorage** sur l’appareil.
8.  Remplissez la playlist en interrogeant le nouveau stockage pour [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)et en appelant [**IWMDMStorage4 :: SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences), en passant le tableau de pointeurs **IWMDMStorage** recueillis à l’étape 4.
9.  Enfin, créez un nouvel objet CItemData pour stocker la nouvelle playlist sur l’appareil, initialisez-le avec le nouveau stockage et appelez CDevFiles :: AddItem pour l’ajouter au volet CDevFiles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’application de bureau**](sample-desktop-application.md)
</dt> </dl>

 

 




