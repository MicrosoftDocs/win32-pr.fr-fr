---
title: Création d’un gestionnaire de nettoyage de disque
description: Un axiome et une nouvelle fois dans le monde des ordinateurs est que, quelle que soit la taille de la capacité de stockage de votre ordinateur, vous finira par le remplir.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- gestionnaires de nettoyage de disque
- Nettoyage de disque
- DataDrivenCleaner
- inscription, gestionnaires de nettoyage de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217366c4e7da2d4fc3b53b7cf32ef418916247d3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622275"
---
# <a name="creating-a-disk-cleanup-handler"></a>Création d’un gestionnaire de nettoyage de disque

Un axiome et une nouvelle fois dans le monde des ordinateurs est que, quelle que soit la taille de la capacité de stockage de votre ordinateur, vous finira par le remplir. Bien que la taille moyenne du disque dur d’un ordinateur ait considérablement augmenté au fil du temps, les applications ont également augmenté en conséquence, ce qui permet aux utilisateurs de rechercher des moyens de créer plus d’espace libre sur le disque dur. L’espace disponible est également réduit par le nombre de fichiers temporaires créés par les applications pour des raisons de sauvegarde ou de performances. Lorsque l’espace disque devient faible, il devient nécessaire de réduire la quantité d’espace utilisée par les applications. L’espace disque peut être libéré à l’aide de différents moyens, y compris les éléments suivants :

-   Suppression des fichiers.
-   Compression des fichiers.
-   Déplacement de fichiers vers un support de sauvegarde.
-   Transfert de fichiers vers un serveur distant.

Les fichiers qui sont de bons candidats au nettoyage sont les suivants :

-   Fichiers dont l’utilisateur n’aura plus besoin.
-   Fichiers temporaires qui existent uniquement pour des raisons de performances.
-   Fichiers qui peuvent être restaurés, le cas échéant, à partir d’un CD d’installation.
-   Fichiers de données qui ont peut-être été remplacés par des versions plus récentes, comme les anciens fichiers de sauvegarde.
-   Fichiers plus anciens qui n’ont pas été utilisés à long terme.

La suppression est particulièrement appropriée pour les fichiers dont l’utilisateur n’aura jamais besoin, par exemple, les fichiers qui sont temporairement mis en cache pour des raisons de performances. La suppression est également appropriée pour les fichiers qui sont facilement restaurés, tels que les fichiers graphiques qui peuvent être rechargées à partir d’un CD d’installation. Les fichiers dont l’utilisateur peut avoir besoin plus tard ou qui serait difficile à reconstruire sont des candidats plus adaptés à la compression ou à la sauvegarde.

L’utilisation d’un utilisateur pour nettoyer manuellement le système de fichiers n’est pas une bonne solution. L’utilisateur peut ne pas savoir où de nombreux fichiers se trouvent ou comment reconnaître ceux qui peuvent être supprimés en toute sécurité. En outre, il existe un risque que l’utilisateur puisse supprimer des fichiers essentiels.

Les facettes suivantes de l’utilitaire de nettoyage de disque sont présentées dans cette rubrique.

-   [utilitaire de nettoyage de disque Windows](#the-windows-disk-cleanup-utility)
-   [Notions de base de l’implémentation](#implementation-basics)
    -   [Initialiser/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Purge](#purge)
    -   [Désactivation](#deactivate)
-   [Inscription d’un gestionnaire de nettoyage de disque](#registering-a-disk-cleanup-handler)
    -   [Inscription du CLSID d’un gestionnaire](#registering-a-handlers-clsid)
    -   [Inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : général](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : Windows systèmes 2000 ou versions ultérieures](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Utilisation de l’objet DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Exemple d’inscription d’un gestionnaire de nettoyage de disque](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>utilitaire de nettoyage de disque Windows

à partir de Windows 98, le système d’exploitation Windows comprend le nettoyage de disque, un utilitaire qui permet à l’utilisateur de gérer plus facilement l’espace disque disponible. L’utilitaire de nettoyage de disque est conçu pour libérer autant d’espace disque que possible et réduire le risque que l’utilisateur supprime accidentellement des fichiers essentiels.

Le nettoyage de disque peut être lancé de trois manières.

-   L’utilisateur peut lancer le nettoyage de disque en cliquant sur **Démarrer**. pointant sur **tous les programmes**, **accessoires** et **Outils système**; puis cliquez sur **nettoyage de disque**.
-   Le système avertit l’utilisateur qu’une boîte de message indiquant que l’espace disque inutilisé a atteint le mode critique. Le seuil de mode critique pour un lecteur supérieur à 2,25 gigaoctets (Go) est de 200 mégaoctets (Mo). Les avertissements suivants sont donnés à 80, 50 et 1 Mo. L’utilisateur a la possibilité de libérer manuellement de l’espace disque ou de démarrer l’utilitaire de nettoyage de disque.
-   l’utilisateur peut disposer de l’assistant tâche planifiée Windows (appelé assistant Maintenance sur les anciens systèmes) pour exécuter automatiquement l’utilitaire de nettoyage de disque à des heures planifiées.

Le défi de base inhérent au nettoyage de disque consiste à libérer autant d’espace disque que possible sans supprimer les fichiers essentiels. Étant donné qu’il n’existe pas de méthode standard pour marquer les fichiers à nettoyer, aucune application ne peut détecter et nettoyer tous les fichiers non essentiels de manière fiable. L’utilitaire de nettoyage de disque résout ce problème en fractionnant l’opération de nettoyage entre un *Gestionnaire de nettoyage de disque* unique et une collection de gestionnaires de nettoyage de *disque*.

Lorsque l’utilitaire de nettoyage de disque est exécuté, l’utilisateur voit la boîte de dialogue suivante. (S’il existe plus d’un disque ou d’une partition de disque sur l’ordinateur, l’utilisateur est d’abord invité à choisir un lecteur avant que cette boîte de dialogue ne s’affiche.)

![capture d’écran de la boîte de dialogue nettoyer](images/cleanup1.png)

Le gestionnaire de nettoyage de disque fait partie du système d’exploitation. Il affiche la boîte de dialogue illustrée dans l’illustration précédente, gère l’entrée d’utilisateur et gère l’opération de nettoyage. La sélection et le nettoyage réels des fichiers inutiles sont effectués par les gestionnaires de nettoyage de disque individuels indiqués dans la zone de liste du gestionnaire de nettoyage de disque. L’utilisateur a la possibilité d’activer ou de désactiver des gestionnaires individuels en activant ou en désactivant leur case à cocher dans l’interface utilisateur du gestionnaire de nettoyage de disque.

Chaque gestionnaire est responsable d’un ensemble bien défini de fichiers. Par exemple, le gestionnaire sélectionné dans l’illustration est responsable du nettoyage des fichiers programmes téléchargés. Le gestionnaire sélectionné dans l’illustration fournit également un bouton **afficher les fichiers** . en cliquant sur le bouton, l’utilisateur peut demander que le gestionnaire affiche une interface utilisateur en général une fenêtre de Windows Explorer qui permet à l’utilisateur de spécifier les fichiers ou classes de fichiers à nettoyer.

bien que Windows soit fourni avec un certain nombre de gestionnaires de nettoyage de disque, ils ne sont pas conçus pour gérer les fichiers générés par d’autres applications. Au lieu de cela, le gestionnaire de nettoyage de disque est conçu pour être flexible et extensible en permettant à n’importe quel développeur d’implémenter et d’inscrire son propre gestionnaire de nettoyage de disque. N’importe quel développeur peut étendre les services de nettoyage de disque disponibles en implémentant et en inscrivant un gestionnaire de nettoyage de disque.

Toutes les applications qui produisent des fichiers temporaires peuvent et doivent implémenter et enregistrer un gestionnaire de nettoyage de disque. Cela offre aux utilisateurs un moyen pratique et fiable de gérer les fichiers temporaires de l’application. Lorsque vous implémentez le gestionnaire, vous pouvez décider quels fichiers sont affectés et déterminer la façon dont le nettoyage réel se produit.

## <a name="implementation-basics"></a>Notions de base de l’implémentation

Les gestionnaires de nettoyage sont des objets COM (Component Object Model) du serveur in-process. Windows fournit un objet de gestionnaire existant appelé DataDrivenCleaner pour votre utilisation. Vous pouvez également choisir d’implémenter un gestionnaire vous-même pour plus de flexibilité. Ces objets vous permettent ensuite de spécifier comment sélectionner des fichiers, l’espace disque disponible et, dans le cas d’un gestionnaire implémenté, d’afficher l’interface utilisateur facultative pour un contrôle plus granulaire. Cette section traite de l’implémentation de votre propre gestionnaire. Pour plus d’informations sur l’utilisation de l’objet DataDrivenCleaner, consultez [utilisation de l’objet DataDrivenCleaner](#using-the-datadrivencleaner-object).

Un gestionnaire de nettoyage de disque doit effectuer ces cinq tâches de base.

-   Initialise l’objet de gestionnaire.
-   Analysez le disque pour déterminer la quantité d’espace disque pouvant être libérée.
-   Affichez l’interface utilisateur pour obtenir des commentaires de l’utilisateur sur les fichiers à nettoyer. (facultatif)
-   Effectuez le nettoyage.
-   Arrêter.

pour autoriser le gestionnaire de nettoyage de disque à gérer ces tâches, un gestionnaire doit exporter [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) pour Windows 98 ou [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) pour Windows Millennium Edition (Windows Me), Windows 2000 et Windows XP. Étant donné que **IEmptyVolumeCache2** hérite de **IEmptyVolumeCache**, l’ajout de la méthode supplémentaire **InitializeEx**, relativement peu de travail supplémentaire est requis pour implémenter les deux. À moins que votre gestionnaire ne soit destiné à un seul de ces systèmes d’exploitation, il doit exporter les deux interfaces.

Pour exporter ces interfaces, vous devez implémenter ces méthodes correspondant aux cinq tâches de base.

-   [Initialiser/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Purge](#purge)
-   [Désactivation](#deactivate)

### <a name="initializeinitializeex"></a>Initialiser/InitializeEx

Les deux méthodes d’initialisation, qui sont assez similaires, sont appelées lors de l’exécution de l’utilitaire de nettoyage de disque. le gestionnaire de nettoyage de disque Windows 98 appelle la méthode [**IEmptyVolumeCache :: initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) d’un gestionnaire. le gestionnaire de nettoyage de disque Windows Millennium edition (Windows Me), Windows 2000 ou Windows XP, en revanche, tente d’abord d’appeler [**IEmptyVolumeCache2 :: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) et utilise uniquement **IEmptyVolumeCache :: initialize** si [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) n’est pas exposé par le gestionnaire. Le gestionnaire de nettoyage de disque transmet des informations à la méthode, telles que la clé de Registre du gestionnaire et le volume de disque à nettoyer.

L’une ou l’autre méthode peut retourner plusieurs chaînes d’affichage et définir un ou plusieurs indicateurs. La principale différence entre les deux méthodes est la façon dont le texte affiché dans le gestionnaire de nettoyage de disque est géré. Les trois chaînes suivantes sont affectées.



| String       | Objectif                                                                            | Initialiser                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Nom d’affichage | Nom du gestionnaire affiché dans la zone de liste du gestionnaire de nettoyage de disque.               | Si *ppwszDisplayName* a la valeur **null**, la valeur par défaut est récupérée à partir du Registre. | Une chaîne correctement localisée doit être spécifiée dans *ppwszDisplayName* aucune valeur de Registre n’est utilisée. |
| Description  | Texte descriptif affiché sous la zone de liste lorsque le nom du gestionnaire est sélectionné. | Si *ppwszDescription* a la valeur **null**, la valeur par défaut est récupérée à partir du Registre. | Une chaîne correctement localisée doit être spécifiée dans *ppwszDescription* aucune valeur de Registre n’est utilisée. |
| Texte du bouton  | Texte pour le bouton facultatif qui permet aux utilisateurs d’afficher l’interface utilisateur du gestionnaire.        | Aucun paramètre disponible. Doit être spécifié dans le registre.                           | Une chaîne correctement localisée doit être spécifiée dans *ppwszBtnText* aucune valeur de Registre n’est utilisée.     |



 

Le paramètre *pdwFlags* trouvé dans les deux méthodes d’initialisation reconnaît le même jeu d’indicateurs. Deux de ces indicateurs sont passés à la méthode par le gestionnaire de nettoyage de disque.

-   **EVCF \_ SETTINGSMODE**

    Si le gestionnaire de nettoyage de disque est exécuté selon une planification, il définit l’indicateur **EVCF \_ SETTINGSMODE** . Si cet indicateur est défini, le gestionnaire de nettoyage de disque n’appelle pas les méthodes [GetSpaceUsed](#getspaceused), [purge](#purge)ou [showProperties](#showproperties) . La méthode [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) ou [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) du gestionnaire doit gérer toutes les tâches normalement effectuées par [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) et [**purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Étant donné qu’il n’y a aucune possibilité de commentaires de la part de l’utilisateur, seuls les fichiers dont le nettoyage est extrêmement sûr doivent être affectés. Vous devez ignorer le paramètre *pcwszVolume* de la méthode d’initialisation et nettoyer les fichiers inutiles, quel que soit le lecteur sur lequel ils se trouvent.

-   **EVCF \_ OUTOFDISKSPACE**

    Si l’indicateur **EVCF \_ OUTOFDISKSPACE** est défini, l’espace disque de l’utilisateur est très faible. Le gestionnaire doit être agressif en ce qui concerne la suppression de fichiers, même si cela entraîne une perte de performances. Toutefois, le gestionnaire ne doit évidemment pas supprimer les fichiers qui provoqueraient l’échec d’une application ou la perte de données par l’utilisateur.

Les indicateurs restants sont définis par le gestionnaire de nettoyage de disque et retournés au gestionnaire de nettoyage de disque. Pour plus d’informations, consultez les pages de référence des méthodes pour [**IEmptyVolumeCache :: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) et [**IEmptyVolumeCache2 :: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Affichez le gestionnaire dans la zone de liste du gestionnaire de nettoyage de disque uniquement si la valeur retournée par [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indique que le gestionnaire peut libérer de l’espace disque.

-   EVCF \_ ENABLEBYDEFAULT

    Spécifie que le gestionnaire est activé par défaut. Elle s’exécute chaque fois qu’un nettoyage de disque a lieu, sauf si l’utilisateur la désactive en désactivant sa case à cocher dans la liste des gestionnaires du gestionnaire de nettoyage de disque.

-   EVCF \_ ENABLEBYDEFAULT \_ auto

    Spécifie que le gestionnaire est automatiquement activé pour s’exécuter pendant les nettoyages planifiés.

-   EVCF \_ HASSETTINGS

    Définissez cet indicateur si votre gestionnaire a une interface utilisateur à afficher. En réponse, le gestionnaire de nettoyage de disque affiche un bouton lorsque ce gestionnaire est sélectionné dans la zone de liste. Si vous cliquez sur ce bouton, le gestionnaire de nettoyage de disque appelle [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Supprimez le nom du gestionnaire de la liste des gestionnaires disponibles une fois que le gestionnaire a été exécuté une fois. Les informations du Registre du gestionnaire sont également supprimées.

### <a name="getspaceused"></a>GetSpaceUsed

Le gestionnaire de nettoyage de disque appelle cette méthode pour déterminer la quantité d’espace qu’un gestionnaire de nettoyage de disque peut potentiellement libérer. Le gestionnaire de nettoyage de disque affiche ensuite cette valeur à droite du nom du gestionnaire dans la zone de liste. Cette opération est effectuée sur tous les gestionnaires inscrits auprès du gestionnaire de nettoyage de disque lorsque le gestionnaire est lancé et avant l’affichage de l’interface utilisateur principale du gestionnaire. Quand [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) est appelé, le gestionnaire doit analyser les fichiers dont il est responsable, déterminer ceux qui sont des candidats aux nettoyages et retourner la quantité d’espace disque qu’il peut libérer.

Étant donné que l’analyse peut être un processus long, le gestionnaire de nettoyage de disque utilise le paramètre *PICB* de cette méthode pour passer un pointeur vers une interface [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) . Le gestionnaire utilise l’interface régulièrement pendant l’analyse pour appeler [**IEmptyVolumeCacheCallBack :: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), qui remplit deux fonctions.

-   Permet au gestionnaire de nettoyage de disque de mettre à jour une barre de progression, en informant l’utilisateur de la progression de l’analyse.
-   Notifie le gestionnaire d’arrêt de l’analyse dans le cas où l’utilisateur clique sur le bouton **Annuler** de la fenêtre de progression. Cet événement de bouton n’est pas communiqué directement au gestionnaire. au lieu de cela, le gestionnaire de nettoyage de disque renvoie E \_ Abort la prochaine fois que [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) appelle [**IEmptyVolumeCacheCallBack :: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties

avant de commencer le nettoyage, le gestionnaire peut afficher une interface utilisateur généralement sous la forme d’une fenêtre d’explorateur de Windows qui permet à l’utilisateur d’afficher la liste des fichiers ou des classes de fichiers sélectionnés pour être nettoyés par le gestionnaire. Si le gestionnaire définit l’indicateur **EVCF \_ HASSETTINGS** lorsque [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) ou [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) est appelé, l’utilisateur peut demander l’interface utilisateur en cliquant sur le bouton affiché à cet effet dans le gestionnaire de nettoyage de disque. Le texte du bouton varie d’un gestionnaire à un gestionnaire, mais les noms « afficher les fichiers », « afficher les pages » et « options » sont des étiquettes courantes.

Lorsque vous cliquez sur le bouton, le gestionnaire de nettoyage de disque appelle [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) pour inviter le gestionnaire à afficher l’interface utilisateur. L’interface utilisateur doit être créée en tant qu’enfant de la fenêtre dont le handle est passé dans le paramètre *HWND* de la méthode **showProperties** .

### <a name="purge"></a>Purge

Le gestionnaire de nettoyage de disque appelle la méthode de [**vidage**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) du gestionnaire pour définir le nettoyage en mouvement. Le paramètre *PICB* de la méthode est un pointeur vers l’interface [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) du gestionnaire de nettoyage de disque. Comme avec la méthode [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , le gestionnaire doit utiliser l’interface de rappel régulièrement pour signaler sa progression et demander au gestionnaire de nettoyage de disque si l’utilisateur a cliqué sur **Annuler**. Toutefois, Notez que la méthode de **vidage** doit appeler [**IEmptyVolumeCacheCallBack ::P urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), et non [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Désactivation

La méthode [**Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) est appelée lors de la préparation de l’arrêt du gestionnaire de nettoyage de disque. Le gestionnaire doit effectuer les tâches de nettoyage nécessaires et retourner. Si vous ne souhaitez pas que le gestionnaire soit réexécuté, définissez l’indicateur **EVCF \_ REMOVEFROMLIST** dans le paramètre *pdwFlags* de la méthode d’initialisation. Si cet indicateur est défini, le gestionnaire de nettoyage de disque supprime le gestionnaire de sa liste et supprime les entrées de Registre du gestionnaire. Vous devez rajouter les entrées de Registre pour exécuter à nouveau le gestionnaire. Cet indicateur est généralement utilisé pour les gestionnaires qui ne sont exécutés qu’une seule fois.

## <a name="registering-a-disk-cleanup-handler"></a>Inscription d’un gestionnaire de nettoyage de disque

pour ajouter un gestionnaire à la liste du gestionnaire de nettoyage de disque, certaines clés et valeurs doivent être ajoutées au registre Windows.

-   [Inscription du CLSID d’un gestionnaire](#registering-a-handlers-clsid)
-   [Inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : général](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : Windows systèmes 2000 ou versions ultérieures](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Utilisation de l’objet DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Exemple d’inscription d’un gestionnaire de nettoyage de disque](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Inscription du CLSID d’un gestionnaire

Comme pour tous les objets COM, le GUID et la DLL de l’objet Handler doivent être enregistrés sous la clé **CLSID** dans la racine de la **\_ classe \_ HKEY**. Vous pouvez également enregistrer une icône qui est affichée en regard du nom du gestionnaire dans la zone de liste du gestionnaire de nettoyage de disque, mais cette option est facultative. L’exemple suivant montre les clés, les valeurs et les données impliquées.

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : général

Pour terminer l’inscription, un gestionnaire doit ajouter une clé contenant ses caractéristiques, comme indiqué ici. Le reste de cette section décrit le contenu de cette clé.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

En général, le nom de la clé contenant les informations d’un gestionnaire est nommé pour le type de fichier qu’il gère, par exemple les **fichiers programmes téléchargés**, mais ce n’est pas obligatoire. Le tableau suivant détaille les valeurs possibles trouvées sous cette clé.

> [!Note]  
> Seule la valeur par défaut spécifiant l’identificateur de classe (CLSID) du gestionnaire est obligatoire. toutes les autres valeurs sont facultatives.

 



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Type</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valeur par défaut</td>
<td>REG_SZ</td>
<td>CLSID du gestionnaire enregistré sous <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Texte du bouton facultatif sur lequel les utilisateurs peuvent cliquer pour afficher l’interface utilisateur du gestionnaire. Le caractère & peut être placé avant un caractère pour affecter un raccourci clavier pour le bouton. La valeur AdvancedButtonText est ignorée par les gestionnaires exposant <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2 :: InitializeEx</strong></a>.</td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Ligne de commande spécifiant un fichier exécutable et des paramètres de ligne de commande facultatifs. Cette ligne de commande est exécutée à la fin du nettoyage de disque.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Identificateur indépendant du système pour un dossier spécial à inclure dans la recherche de fichiers. Cette valeur doit être entrée sous la forme d’une valeur numérique pour l’instance, 0x0000001c plutôt que CSIDL_LOCAL_APPDATA. Pour obtenir la liste des valeurs possibles, consultez <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Une seule valeur peut être utilisée.<br/> Si la valeur du dossier est spécifiée, l’emplacement indiqué par la valeur CSIDL est ajouté à ces informations pour composer un chemin de recherche. Par exemple, considérez le scénario suivant.<br/>
<ul>
<li>La valeur CSIDL est spécifiée en tant que 0x0000000d (CSIDL_MYMUSIC)</li>
<li>votre dossier mes Musique se trouve dans C:\Documents and Paramètres \<em>username</em>\mes Musique</li>
<li>La valeur du dossier contient &quot; Jazz\Singers&quot;</li>
</ul>
le résultat de ce scénario est que le gestionnaire de nettoyage de disque recherche le dossier C:\Documents and Paramètres \<em>username</em>\mes Musique \Jazz\Singers. Notez que la barre oblique qui précède la valeur du dossier est ajoutée si elle n’est pas présente.<br/></td>
</tr>
<tr class="odd">
<td>Description</td>
<td>REG_SZ</td>
<td>Texte descriptif affiché sous la zone de liste du gestionnaire de nettoyage de disque lorsque le nom du gestionnaire est sélectionné. Ici, vous pouvez expliquer ce que fait le gestionnaire, les fichiers dont il se réagit et tout autre renseignement à l’utilisateur. Si <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2 :: InitializeEx</strong></a> n’est pas exposé par le gestionnaire, ce texte peut être substitué par le biais de la méthode <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache :: Initialize</strong></a> du gestionnaire en spécifiant une autre chaîne dans le paramètre <em>ppwszDescription</em> lorsque la méthode est appelée.</td>
</tr>
<tr class="even">
<td>Affichage</td>
<td>REG_SZ</td>
<td>Nom du gestionnaire à afficher dans la zone de liste du gestionnaire de nettoyage de disque. Si <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2 :: InitializeEx</strong></a> n’est pas exposé par le gestionnaire, ce texte peut être substitué par le biais de la méthode <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache :: Initialize</strong></a> du gestionnaire en spécifiant une autre chaîne dans le paramètre <em>ppwszDisplayName</em> lorsque la méthode est appelée.</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ ou REG_MULTI_SZ</td>
<td>Liste des fichiers recherchés et nettoyés par ce gestionnaire. Vous pouvez spécifier des caractères génériques à l’aide de l' ? ou * caractères. Si la valeur est de type REG_SZ, plusieurs extensions sont séparées à l’aide du | ou : caractères, sans espace de chaque côté.<br/> Si l’indicateur DDEVCF_REMOVEDIRS est défini dans la valeur flags, ces valeurs peuvent spécifier des noms de répertoire ainsi que des fichiers.<br/></td>
</tr>
<tr class="even">
<td>Indicateurs</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Indicateurs contrôlant les éléments de la procédure de recherche et de nettoyage. Une ou plusieurs des valeurs suivantes.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Recherchez et supprimez de manière récursive.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Après l’exécution du gestionnaire, supprimez-le du Registre.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Supprimer les fichiers qui répondent aux critères de recherche, même s’ils sont en lecture seule.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Supprimer les fichiers qui répondent aux critères de recherche, même s’il s’agit de fichiers système.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Supprimer les fichiers qui répondent aux critères de recherche, même s’il s’agit de fichiers cachés.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Ne pas afficher ce gestionnaire dans le gestionnaire de nettoyage de disque si aucun fichier ne correspond à ses critères de recherche.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Faire correspondre la valeur FileList aux répertoires et supprimer les correspondances et tous leurs sous-répertoires.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Exécutez ce gestionnaire uniquement si l’espace disque disponible est tombé en dessous de la valeur critique, déterminé par le gestionnaire de nettoyage de disque qui définit l’indicateur de EVCF_OUTOFDISKSPACE via <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache :: Initialize</strong></a> ou <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2 :: InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Supprime le répertoire parent des fichiers spécifiés une fois le nettoyeur exécuté.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Utilisez la valeur LastAccess, si elle est fournie, pour déterminer les fichiers qui doivent être nettoyés. Cet indicateur est ignoré lors de l’utilisation de <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> toute valeur LastAccess fournie est toujours utilisée.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Dossier</td>
<td>REG_SZ, REG_MULTI_SZ ou REG_EXPAND_SZ</td>
<td>Dossier ou dossiers spécifiques dans lesquels rechercher les éléments correspondant aux entrées de la valeur FileList. Vous pouvez spécifier des caractères génériques à l’aide de l' ? ou * caractères. Si la valeur est de type REG_SZ, plusieurs noms de dossiers sont séparés à l’aide du | caractère, sans espaces de part et d’autre.<br/> Si une valeur CSIDL est présente, un seul dossier peut être spécifié dans cette valeur. L’emplacement indiqué par la valeur CSIDL est ajouté au début de ce chemin d’accès de dossier pour composer un chemin de recherche. Pour obtenir un exemple, consultez la description de la valeur CSIDL.<br/> si cette valeur est absente de Windows Vista Service Pack 1 (SP1) et versions ultérieures, le gestionnaire de nettoyage est ignoré et retourne S_FALSE lors de l’initialisation.<br/> si cette valeur est absente de la version d’origine de Windows Vista et versions antérieures, le dossier racine du volume actuel est utilisé. L’indicateur DDEVCF_DOSUBDIRS est nécessaire dans ce cas pour effectuer une recherche dans l’ensemble du lecteur. Sans cela, seul le dossier racine est recherché.<br/> Vous devez spécifier un ou des lecteurs. Cela peut être fourni par le biais de la valeur CSIDL ou par le biais d’une chaîne REG_EXPAND_SZ. En excluant ces options, le lecteur à rechercher doit être spécifié dans le nom du dossier. Utilisez ?: pour rechercher le dossier sur le lecteur actif.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ ou REG_EXPAND_SZ</td>
<td>Chemin d’accès à la ressource à partir de laquelle obtenir une icône à utiliser en association avec le gestionnaire.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Nombre de jours qui doivent s’écouler depuis le dernier accès à un fichier ou lors de la création d’un répertoire pour ce fichier ou ce répertoire en vue du nettoyage.</td>
</tr>
<tr class="even">
<td>Priority</td>
<td>REG_DWORD ou REG_BINARY</td>
<td>Détermine l’ordre d’exécution du gestionnaire par rapport à d’autres gestionnaires. Plus le nombre est élevé, plus il est haut dans le processus exécuté par le gestionnaire. Il n’existe aucune plage définie. aucun nombre n’est acceptable.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>CLSID d’une ressource utilisée pour fournir du texte localisé pour le nom complet, la description et le texte du bouton. cette ressource est utile dans le cas où un gestionnaire n’implémente pas <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> et que le gestionnaire est exécuté sous Microsoft Windows NT ou Windows XP.<br/> Le gestionnaire de nettoyage de disque vérifie d’abord si la routine d’initialisation du gestionnaire a retourné ces chaînes, comme c’est le cas lors de l’implémentation de <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> . À l’échec, le gestionnaire se transforme en un conteneur de propriétés nommé dans cette valeur. Si aucun n’a été fourni, il récupère le texte à partir du Registre.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>En exécutant le fichier exécutable du gestionnaire de nettoyage de disque Cleanmgr.exe à partir d’une ligne de commande, vous pouvez déclarer des <em>profils</em>de nettoyage. Ces profils sont composés d’un sous-ensemble des gestionnaires disponibles et reçoivent une étiquette numérique unique. Cela vous permet d’automatiser l’exécution de différents jeux de gestionnaires à des moments différents.<br/> La ligne de commande &quot;cleanmgr.exe/sageset :<strong>nnnn</strong> &quot; , où <strong>nnnn</strong> est une étiquette numérique unique, affiche une interface utilisateur qui vous permet de choisir les gestionnaires à inclure dans ce profil. En plus de définir le profil, le paramètre sageset écrit également une valeur nommée StateFlags<strong>nnnn</strong>, où <strong>nnnn</strong> est l’étiquette que vous avez utilisée dans le paramètre, à toutes les sous-clés sous <strong>VolumeCaches</strong>. Il existe deux valeurs de données possibles pour ces entrées.
<ul>
<li>0 : n’exécutez pas ce gestionnaire lors de l’exécution de ce profil.</li>
<li>2 : inclure ce gestionnaire lors de l’exécution de ce profil.</li>
</ul>
<br/> Par exemple, supposons que la ligne de commande &quot;cleanmgr.exe/sageset : 1234 &quot; soit exécutée. Dans l’interface utilisateur présentée, l’utilisateur choisit <strong>fichiers programmes téléchargés</strong>, mais ne choisit pas <strong>fichiers Internet temporaires</strong>. Les valeurs suivantes sont ensuite écrites dans le registre.<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> La ligne &quot; de commandecleanmgr.exe/sagerun :<strong>nnnn</strong> &quot; , où la valeur de <strong>nnnn</strong> correspond à l’étiquette déclarée avec le paramètre sageset, exécute tous les gestionnaires sélectionnés dans ce profil.<br/> Une valeur StateFlags générique est écrite dans le registre lorsque le nettoyage de disque est exécuté normalement. Cette valeur stocke simplement l’État (activé ou désactivé) du gestionnaire la dernière fois qu’il a été présenté en tant qu’option à l’utilisateur. Il existe deux valeurs de données possibles pour ces entrées.
<ul>
<li>0 : le gestionnaire n’a pas été sélectionné.</li>
<li>1 : le gestionnaire a été sélectionné.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : Windows systèmes 2000 ou versions ultérieures

La spécification du texte affiché dans le registre peut compliquer la localisation des logiciels. pour cette raison, Windows 2000 et Windows XP prennent en charge l’interface [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) avec sa méthode d’initialisation préférée [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). sous Windows 2000 ou une version ultérieure, une tentative est toujours effectuée pour appeler **IEmptyVolumeCache2 :: InitializeEx** avant [**IEmptyVolumeCache :: initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). Le système utilise uniquement **Initialize** pour initialiser un gestionnaire si **IEmptyVolumeCache2** n’est pas exposé.

en ce qui concerne le registre, la seule différence sous Windows 2000 ou version ultérieure est que vous pouvez omettre les valeurs AdvancedButtonText, Display et Description lorsque [**IEmptyVolumeCache2 :: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) est exposé par le gestionnaire. Ces valeurs, contenant du texte correctement localisé, sont fournies au gestionnaire de nettoyage de disque lors de l’appel de **InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Utilisation de l’objet DataDrivenCleaner

Un gestionnaire de nettoyage de disque de base, appelé DataDrivenCleaner, est fourni par le système d’exploitation. Pour utiliser cet objet en tant que gestionnaire plutôt que d’implémenter le vôtre, utilisez le CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} comme valeur par défaut pour la sous-clé du gestionnaire sous **VolumeCaches** , comme décrit dans [inscription d’un gestionnaire à l’aide du gestionnaire de nettoyage de disque : général](#registering-a-handler-with-the-disk-cleanup-manager-general).

DataDrivenCleaner n’expose pas [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), de sorte que les valeurs d’affichage et de description sont fournies par le biais du Registre. Lorsque vous déclarez ces chaînes, sachez que cela peut entraîner des problèmes de localisation. Le texte localisé peut être fourni via la valeur PropertyBag. La valeur AdvancedButtonText est ignorée, car aucune interface utilisateur, et donc aucun bouton pour l’afficher, est disponible pour ce gestionnaire.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Exemple d’inscription d’un gestionnaire de nettoyage de disque

l’exemple suivant montre un exemple d’inscription pour un gestionnaire de nettoyage de disque implémenté par la société Téléphone. ce gestionnaire implémente à la fois [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) et [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), et fournit donc des valeurs AdvancedButtonText, Description et Display en cas d’utilisation sur un ordinateur exécutant Windows 98. le gestionnaire combine les valeurs de l’option CSIDL et du dossier pour rechercher des fichiers dans les fichiers de programme C : \\ \\ du Téléphone répertoire temporaire de la société \\ , et l' \_ indicateur DDEVCF DOSUBDIRS est défini de sorte que la recherche s’effectue également dans ses sous-répertoires. Seuls les fichiers avec les extensions. tmp et. TPC sont pris en compte pour le nettoyage, et l' \_ indicateur DDEVCF Private \_ LASTACCESS est défini de sorte que seuls les fichiers qui n’ont pas été consultés depuis 14 jours ou plus soient pris en compte. L' \_ indicateur DDEVCF DONTSHOWIFZERO est également défini de sorte que le gestionnaire n’apparaisse pas dans la liste, sauf s’il a trouvé des candidats aux nettoyages.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

