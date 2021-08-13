---
description: Découvrez comment créer un moteur de synchronisation de fichiers Cloud qui utilise des fichiers d’espace réservé à l’aide de l’API de fichiers Cloud.
title: Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551572"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé

Un moteur de synchronisation est un service qui synchronise les fichiers, généralement entre un hôte distant et un client local. les moteurs de synchronisation sur Windows présentent souvent ces fichiers à l’utilisateur par le biais du système de fichiers Windows et de l’explorateur de fichiers. avant Windows 10, la version 1709 de la prise en charge du moteur de synchronisation dans Windows était limitée à des surfaces ad hoc indépendantes du scénario, telles que le volet de navigation de l’explorateur de fichiers, la barre d’état système Windows et (pour les applications plus techniques) des pilotes de filtre de système de fichiers.

Windows 10 version 1709 (également appelée « mise à jour des créateurs de automne ») a introduit l' *API de fichiers cloud*. Cette API est une nouvelle plateforme qui formalise la prise en charge des moteurs de synchronisation. L’API de fichiers Cloud prend en charge les moteurs de synchronisation d’une manière qui offre de nombreux nouveaux avantages aux développeurs et aux utilisateurs finaux.

l’api de fichiers cloud contient les api Win32 natives et les api Windows Runtime (WinRT) suivantes :

* [API de filtre Cloud](cloud-filter-reference.md): cette API Win32 native fournit des fonctionnalités à la limite entre le mode utilisateur et le système de fichiers. Cette API gère la création et la gestion de fichiers et de répertoires d’espace réservé.
* [Windows. Stockage. Espace de noms du fournisseur](/uwp/api/windows.storage.provider): cette API WinRT permet aux applications de configurer le fournisseur de stockage cloud et d’inscrire la racine de synchronisation auprès du système d’exploitation.

> [!NOTE]
> L’API de fichiers Cloud ne prend pas actuellement en charge l’implémentation de moteurs de synchronisation Cloud dans des applications UWP. Les moteurs de synchronisation Cloud doivent être implémentés dans les applications de bureau.

## <a name="supported-features"></a>Fonctionnalités prises en charge

L’API de fichiers Cloud fournit les fonctionnalités suivantes pour créer des moteurs de synchronisation Cloud.

### <a name="placeholder-files"></a>Fichiers d’espace réservé

* Les moteurs de synchronisation peuvent créer des fichiers d’espace réservé qui consomment uniquement 1 Ko de stockage pour l’en-tête du système de fichiers, et qui sont automatiquement alimentés en fichiers complets dans des conditions d’utilisation normales. fichiers d’espace réservé présents en tant que fichiers standard pour les applications et pour les utilisateurs finaux dans le Shell Windows.
* les fichiers d’espace réservé sont intégrés verticalement à partir du noyau de Windows jusqu’au Shell Windows, et la compatibilité des applications avec les fichiers d’espace réservé n’est généralement pas un problème. Que vous utilisiez des API de système de fichiers, l’invite de commandes ou un ordinateur de bureau ou une application UWP pour accéder à un fichier d’espace réservé, le fichier est hydraté sans modification de code supplémentaire et cette application peut utiliser le fichier normalement.
* Les fichiers peuvent exister dans trois États :
  * **Fichier d’espace réservé**: représentation vide du fichier et disponible uniquement si le service de synchronisation est disponible.
  * **Fichier complet**: le fichier a été mis en attente implicitement et peut être mis en attente par le système si de l’espace est nécessaire.
  * **Fichier complet épinglé**: le fichier a été mis en attente explicitement par l’utilisateur via l’Explorateur de fichiers et est assuré d’être disponible hors connexion.

L’illustration suivante montre comment les États d’espace réservé, de remplissage complet et de fichier complet épinglé sont affichés dans l’Explorateur de fichiers.

  ![Exemple de trois États de fichiers dans l’Explorateur de fichiers](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Inscription de la racine de synchronisation standardisée

* L’inscription d’une racine de synchronisation est simple et standardisée. Cela comprend la création d’un nœud de personnalisation dans le volet de navigation de l’Explorateur de fichiers, comme illustré dans la capture d’écran suivante. Les racines peuvent être créées en tant qu’entrées de niveau supérieur individuelles ou en tant qu’enfants d’un regroupement parent.

  ![Exemple d’entrée racine de synchronisation dans l’Explorateur de fichiers](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Intégration de Shell

* Icônes d’État :
  * l’API fichiers cloud fournit des icônes standardisées et automatiques d’état d’hydratation affichées dans l’explorateur de fichiers et sur le bureau Windows.
  * outre les icônes d’état de Windows standard utilisées pour l’état de l’hydratation, vous pouvez fournir des icônes d’état personnalisées pour les propriétés supplémentaires spécifiques au service.
  * Remplace les extensions d’environnement de superposition d’icône héritées.
* Indication de la progression :
  * L’ouverture d’un fichier d’espace réservé qui prend plus de quelques secondes pour être en attente indique la progression de l’attente. La progression est affichée à quelques emplacements en fonction du contexte :
    * Dans une fenêtre de boîte de dialogue du moteur de copie.
    * La progression Inline est affichée en regard du fichier dans l’Explorateur de fichiers.
    * Si le fichier n’est pas ouvert à l’instruction spécifique de l’utilisateur, une notification Toast est présentée pour informer l’utilisateur et fournir un moyen de contrôler l’activité d’alimentation involontaire.
* Miniatures et métadonnées :
  * Les fichiers d’espace réservé peuvent avoir des miniatures riches en service et des métadonnées de fichier étendues pour fournir à l’utilisateur une expérience d’Explorateur de fichiers transparente.
* Volet de navigation de l’Explorateur de fichiers :
  * L’inscription d’une racine de synchronisation avec l’API fichiers Cloud provoque l’affichage de la racine de synchronisation (avec une icône et un nom personnalisé) dans le volet de navigation de l’Explorateur de fichiers.
* Menus contextuels de l’Explorateur de fichiers :
  * L’inscription d’une racine de synchronisation avec l’API fichiers Cloud fournit automatiquement plusieurs verbes (entrées de menu) dans le menu contextuel de l’Explorateur de fichiers qui permettent à l’utilisateur de contrôler l’état d’hydratation de son fichier.
  * des verbes supplémentaires peuvent être ajoutés à cette section du menu contextuel à l’aide d’api compatibles Pont du bureau.
* Contrôle utilisateur de l’hydratation de fichiers :
  * Les utilisateurs contrôlent toujours l’hydratation des fichiers, même si les fichiers ne sont pas alimentés explicitement par l’utilisateur. Un toast interactif est affiché pour l’hydratation en arrière-plan afin d’alerter l’utilisateur et de fournir des options. L’image suivante montre une notification toast pour un fichier hydratation.
    ![Exemple d’un toast interactif affiché pour l’attente de fichiers en arrière-plan](images/file-hydration-interactive-toast.png)
  * si un utilisateur empêche une application d’en bloquer les fichiers par le biais d’un toast interactif, elle peut débloquer l’application dans la page de **téléchargement automatique des fichiers** de **Paramètres**.
    ![Capture d’écran du paramètre de téléchargement automatique des fichiers](images/allow-automatic-file-downloads-setting.png)
* raccordement des opérations du moteur de copie (pris en charge dans Windows 10 insider preview version 19624 et versions ultérieures) :
  * Les fournisseurs de stockage cloud peuvent inscrire un hook de copie de Shell pour analyser les opérations de fichiers au sein de leur racine de synchronisation.
  * Le fournisseur inscrit son raccordement de copie en affectant à la valeur de Registre **CopyHook** sous sa clé de Registre racine de synchronisation le CLSID de l’objet serveur local com. Cet objet serveur local implémente l’interface [IStorageProviderCopyHook](../shell/nn-shobjidl-istorageprovidercopyhook.md) .

### <a name="desktop-bridge"></a>Pont du bureau

* les moteurs de synchronisation utilisant les api de fichiers cloud sont conçus pour utiliser le [Pont du bureau](/windows/uwp/porting/desktop-to-uwp-root) en tant que spécification d’implémentation.

## <a name="cloud-mirror-sample"></a>Exemple de miroir Cloud

L' [exemple Cloud Mirror](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) illustre la création d’une solution qui utilise l’API de fichiers Cloud. Il n’est pas destiné à être utilisé comme code de production. Il manque une gestion fiable des erreurs et il est conçu pour être aussi facilement compréhensible que possible. Il s’agit d’un miroir Cloud, car il reflète simplement un dossier local sur votre disque local. Vous spécifiez un dossier de serveur destiné à représenter votre serveur de fichiers Cloud et un dossier client destiné à spécifier le chemin d’accès racine de synchronisation. Un nœud de niveau supérieur apparaît dans le volet de navigation de l’Explorateur de fichiers appelé **TestStorageProviderDisplayName**, et ce nœud est mappé au dossier client spécifié.

Lorsqu’il s’agit de la synchronisation, il s’agit des éléments qu’un fournisseur de synchronisation de fichiers Cloud entièrement développé doit implémenter :

* Lorsque le fichier racine de synchronisation est simplement un espace réservé, le service est responsable de la copie du contenu du fichier pour l’hydratation. Elle est implémentée dans l’exemple.
* Lorsque le fichier racine de synchronisation est un fichier complet et que le contenu du fichier dans le service Cloud change, le service est chargé de notifier le client de synchronisation local de la modification et le client de synchronisation local doit gérer les fusions en fonction de leurs propres spécifications. Cela n’est pas implémenté dans l’exemple.
* Lorsque le fichier racine de synchronisation est un fichier complet et que le contenu du fichier dans le chemin racine de synchronisation (client local) change, le client de synchronisation local doit notifier le service Cloud et gérer les fusions en fonction de leurs propres spécifications. La notification de modification de fichier local est implémentée dans l’exemple, mais elle ne fait rien.

### <a name="use-the-sample"></a>Utiliser l’exemple

1. Créez deux dossiers sur votre disque dur local. L’un d’eux fera office de serveur et l’autre en tant que client.
2. Ajoutez des fichiers au dossier serveur. Assurez-vous que le dossier client est vide.
3. Ouvrez l’exemple de miroir Cloud dans Visual Studio. Définissez le projet **CloudMirrorPackage** comme projet de démarrage, puis générez et exécutez l’exemple. Lorsque l’exemple vous y invite, entrez les deux chemins d’accès à vos dossiers serveur et client. Après cela, vous verrez une fenêtre de console avec des informations de diagnostic.
4. Ouvrez l’Explorateur de fichiers et vérifiez que vous voyez le nœud **TestStorageProviderDisplayName** et les espaces réservés pour tous les fichiers que vous avez copiés dans le dossier serveur. Pour simuler une application qui tente d’ouvrir des fichiers sans utiliser le sélecteur, copiez plusieurs images dans le dossier serveur. Double-cliquez sur l’un d’entre eux dans votre dossier racine de synchronisation et confirmez qu’il est en attente. ensuite, ouvrez l’application Photos. L’application préchargera les fichiers adjacents en arrière-plan pour augmenter la probabilité que l’utilisateur ne rencontre pas de retards lors de la consultation des autres images. Vous pouvez observer que la mise en attente de l’arrière-plan se produit via des toasts ou dans l’Explorateur de fichiers.
5. Cliquez avec le bouton droit sur un fichier dans l’Explorateur de fichiers pour afficher un menu contextuel et vérifiez que l’élément de menu **test** s’affiche. Cliquez sur cet élément de menu pour afficher une boîte de message.
6. Pour arrêter l’exemple, définissez le focus sur la sortie de la console et appuyez sur **Ctrl-C**. Cela permet de nettoyer l’inscription de la racine de synchronisation afin que le fournisseur soit désinstallé. Si l’exemple se bloque, il est possible que la racine de synchronisation reste inscrite. Cela entraînera le redémarrage de l’Explorateur de fichiers chaque fois que vous cliquerez sur quoi que ce soit, et vous seriez invité à entrer les emplacements fictifs du client et du serveur. Si cela se produit, désinstallez l’exemple d’application **CloudMirrorPackage** sur votre ordinateur.

### <a name="sample-architecture"></a>Exemple d’architecture

L’exemple est délibérément simple. Il utilise des classes statiques pour éviter de passer des pointeurs d’instance. Voici les principales classes de l’exemple :

* **FakeCloudProvider**: cette classe de niveau supérieur contrôle les classes de travail suivantes :
  * **CloudProviderRegistrar**: enregistre les informations de la racine de synchronisation avec le Shell Windows.
  * **Espaces réservés**: génère les fichiers d’espace réservé dans le chemin racine de synchronisation.
  * **ShellServices**: construit les fournisseurs de Shell Windows pour le menu contextuel, les miniatures et d’autres services.
  * **CloudProviderSyncRootWatcher**: instancie un DirectoryWatcher pour surveiller les modifications apportées au chemin d’accès racine de synchronisation et agir sur les modifications.
  * **FileCopierWithProgress**: copie les fichiers du dossier du serveur vers le dossier client, lentement en segments pour simuler leur téléchargement à partir d’un serveur Cloud réel. Fournit une indication de progression afin que les toasts et l’interface utilisateur de l’Explorateur de fichiers affichent l’information sur l’utilisateur.

Outre les classes ci-dessus, l’exemple fournit également plusieurs classes d’assistance pour inviter l’utilisateur à fournir des dossiers et certains utilitaires. **TestExplorerCommandHandler**, **CustomStateProvider**, **ThumbnailProvider** et **uriSource** sont tous des exemples de fournisseurs de services de Shell.

## <a name="cloud-files-api-architecture"></a>Architecture des API de fichiers Cloud

Au cœur de la pile de stockage dans l’API des fichiers Cloud se trouve un pilote de minifiltre de système de fichiers appelé cldflt.sys. Ce pilote agit comme un proxy entre les applications de l’utilisateur et votre moteur de synchronisation. Votre moteur de synchronisation sait comment télécharger et télécharger les données à la demande, alors qu’il est responsable de cldflt.sys à utiliser l’interpréteur de commandes pour présenter des fichiers comme si les données Cloud étaient disponibles localement.

Cldflt.sys prend actuellement en charge uniquement les volumes NTFS, car cela dépend de certaines fonctionnalités propres à NTFS.

Il existe de nombreux pilotes de minifiltre de système de fichiers dans un système qui peuvent être actifs simultanément sur un volume donné. Les pilotes qui sont le plus intéressants pour l’API des fichiers Cloud sont les filtres du système de fichiers antivirus.

Les pilotes de minifiltre du système de fichiers sont gérés et pris en charge par un composant en mode noyau spécial appelé gestionnaire de filtres. Entre autres tâches, le gestionnaire de filtres facilite la communication non filtrée entre les filtres et les composants du mode utilisateur via une construction appelée port de message de filtre.

## <a name="hydration-policies"></a>Stratégies d’hydratation

Windows prend en charge une variété de [stratégies d’hydratation principales](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) et de modificateurs de [stratégie d’hydratation secondaires](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) . Les stratégies de mise en attente principales sont les suivantes :

  **Toujours plein > > progressif complet > partiel**

Les applications et les moteurs de synchronisation peuvent définir la stratégie d’alimentation principale par défaut. S’il n’est pas spécifié, la stratégie d’hydratation par défaut est progressive pour les applications et les moteurs de synchronisation.

La stratégie d’hydratation d’un fichier Cloud est déterminée au moment de l’ouverture du fichier par la formule suivante :

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Supposons, par exemple, que l’utilisateur essaie d’ouvrir un fichier PDF stocké sur le lecteur Cloud Fabrikam à l’aide de la visionneuse PDF contoso, qui ne spécifie pas de stratégie d’hydratation préférée. La stratégie d’hydratation d’application est donc une alimentation progressive, dans ce cas par défaut. Toutefois, étant donné que le lecteur Cloud Fabrikam est un moteur de synchronisation en alimentation complète, la stratégie finale d’hydratation sur le fichier devient une alimentation complète, ce qui entraîne l’alimentation intégrale du fichier au premier accès. Le même résultat se produit dans les cas où le moteur de synchronisation prend en charge l’hydratation progressive, mais la préférence de l’application est l’hydratation complète.

Notez que la stratégie d’alimentation des fichiers ne peut pas être modifiée une fois que le fichier est ouvert.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilité avec les applications qui utilisent des points d’analyse

L’API de fichiers Cloud implémente le système d’espace réservé à l’aide de [points d’analyse](/windows/desktop/FileIO/reparse-points). La fausse idée des points d’analyse est qu’ils sont identiques aux liens symboliques. Cette idée fausse est parfois reflétée dans les implémentations d’application et, par conséquent, de nombreuses applications existantes ont rencontré des erreurs lors de la rencontre d’un point d’analyse.

Pour atténuer ce problème de compatibilité, l’API de fichiers Cloud masque toujours ses points d’analyse à partir de toutes les applications, à l’exception des moteurs de synchronisation et des processus dont l’image principale réside sous **% systemroot%**. Les applications qui comprennent correctement les points d’analyse peuvent forcer la plateforme à exposer des points d’analyse de l’API des fichiers Cloud à l’aide de [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) ou [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).