---
description: Montre comment s’inscrire en tant que fournisseur racine de synchronisation et intégrer un fournisseur de stockage cloud dans le niveau racine du volet de navigation.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: intégrer un fournisseur de Stockage Cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458199"
---
# <a name="integrate-a-cloud-storage-provider"></a>intégrer un fournisseur de Stockage Cloud

Si vous disposez d’un fournisseur de stockage cloud, vous devez effectuer quelques étapes pour fournir une expérience cohérente et préférée pour l’utilisateur. Ces deux opérations s’inscrivent en tant que fournisseur racine de synchronisation et intègrent votre application dans le niveau racine du volet de navigation.

> [!IMPORTANT]
> L’intégration de votre fournisseur de stockage cloud n’est prise en charge qu’à partir de Windows 10.

 

La première chose à faire est de s’inscrire en tant que fournisseur racine de synchronisation. cela permet à l’interpréteur de commandes Windows de connaître votre application et de faire en sorte que votre application soit responsable de la synchronisation des fichiers sous votre racine de synchronisation. Cela permettra également à d’autres applications de savoir que vous synchronisez ces fichiers pour qu’ils puissent répondre de manière appropriée. D’autres applications peuvent ensuite utiliser [**StorageFile. Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) pour afficher [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) et l' [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) de votre application.

Pour vous inscrire en tant que fournisseur racine de synchronisation, vous devez créer plusieurs entrées de registre. Avant de fournir la liste des paires clé-valeur, voici quelques espaces réservés que vous devez remplacer par vos propres données d’application.

-   *\[ ID \] du fournisseur de stockage*: nom de votre fournisseur de stockage cloud. Ce nom doit être cohérent, quelle que soit la version de votre application. OneDrive en est un exemple.
-   *\[ sid \] Windows*: le sid Windows unique qui identifie l’utilisateur. Si votre application prend en charge plusieurs installations pour plusieurs utilisateurs sur un seul ordinateur, ce composant est nécessaire.
-   *\[ ID \] de compte*: identificateur du fournisseur de services pour le compte actuel de cet utilisateur. Certains fournisseurs nécessitent la possibilité de fournir plusieurs racines de synchronisation pour un utilisateur. Un compte professionnel et un compte personnel en sont un exemple. L' *ID de compte* vous permet d’avoir plusieurs comptes inscrits pour un seul utilisateur. Si votre fournisseur prend en charge plusieurs racines de synchronisation par utilisateur, ce composant est nécessaire.

Ces espaces réservés sont combinés pour former l’ID racine de synchronisation. Vous devez placer un **!** caractère entre chacun des espaces réservés lors de la formation de l’ID racine de synchronisation. Voici les paires clé-valeur qui doivent être créées.

-   **HKLM \\ logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] de compte_*_\\ DisplayNameResource_* : pointe vers la ressource dans laquelle l’interpréteur de commandes Windows ou d’autres applications peuvent obtenir un nom convivial pour votre racine de synchronisation.
-   **HKLM \\ logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] de compte_*_\\ IconResource_* : pointe vers la ressource dans laquelle l’interpréteur de commandes Windows ou d’autres applications peuvent obtenir une icône pour votre racine de synchronisation.
-   **HKLM \\ logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ SyncRootManager \\**_\[ storage provider ID \]_*_!_* _\[ Windows SID \]_*_!_* _\[ ID \] de compte_*_\\ UserSyncRoots \\_*_\[ Windows \] SID_ : emplacement sur le disque où se trouve la racine de synchronisation.

En dehors de l’inscription en tant que fournisseur racine de synchronisation, vous souhaitez également que les utilisateurs aient un accès facile aux données que vous fournissez. L’espace de noms de l’Explorateur de fichiers est conçu pour offrir une méthode d’accès facile. La création d’une extension d’espace de noms pour votre fournisseur et son incorporation dans la fenêtre de l’Explorateur de fichiers permet aux utilisateurs d’interagir avec le niveau racine de vos services de la même manière qu’ils sont utilisés avec d’autres éléments de l’Explorateur de fichiers. Cette rubrique explique comment étendre l’espace de noms de l’Explorateur de fichiers afin que votre fournisseur s’affiche au niveau de la racine dans le volet de navigation.

Le volet de navigation de la fenêtre de l’Explorateur de fichiers est la partie de la fenêtre affichée sur le côté gauche. Dans l’image ci-dessous, vous pouvez voir la structure de l’espace de noms pour cet utilisateur. le niveau racine dans le volet de Navigation comprend les objets pour **OneDrive**, **ce PC** et le **réseau**. La procédure suivante permet d’ajouter votre extension au même niveau.

![volet de navigation](images/navigationpane.png)

Pour ajouter votre extension au volet de navigation, vous devez disposer des éléments suivants avant de modifier le registre :

-   Dossier du système de fichiers qui contient les données à afficher à l’utilisateur.

-   Nom de votre service Cloud qui s’affichera dans le volet de navigation. Il peut également s’agir du nom de l’instance si votre service prend en charge plusieurs comptes.

-   Icône identifiable pour votre application.

-   Un CLSID pour votre application. L’une des façons de générer un CLSID pour votre application consiste à utiliser la Uuidgen.exe. Pour plus d’informations sur CLSID, consultez [clé CLSID](../com/clsid-key-hklm.md) .

Les étapes suivantes permettent de modifier le registre afin d’extraire les informations nécessaires dans l’espace de noms de l’Explorateur de fichiers. Les étapes spécifiques effectuent trois opérations.

-   Créez des clés dans le registre pour votre CLSID qui incluent des valeurs pour le nom et l’icône de votre extension, ainsi que d’autres informations qui définissent son comportement.

-   Configurez votre extension pour qu’elle soit intégrée dans le volet de navigation à l’emplacement approprié et avec la visibilité appropriée.

-   Configurez votre extension pour obtenir le comportement attendu pour un élément dans le volet de navigation.

Ces instructions utilisent spécifiquement la commande **reg.exe** , mais vous pouvez utiliser n’importe quel outil de modification du registre de votre choix. Vous pouvez même intégrer ces étapes dans un programme d’installation qui met à jour le registre par programme.

## <a name="instructions"></a>Instructions

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Étape 1 : ajouter votre CLSID et nommer votre extension

Ajoutez le nom de votre extension au Registre sous HKEY \_ Current \_ User. Vous allez également ajouter l’identificateur unique pour cette extension. Il est possible d’ajouter plusieurs extensions par utilisateur, mais dans ce cas, vous aurez besoin d’un nom et d’un identificateur uniques pour chaque extension. Ce nom et cet identificateur doivent être cohérents dans le reste de ces étapes. Dans cet exemple, le nom est *MyCloudStorageApp*.

> [!IMPORTANT]
> L’identificateur fourni (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) dans ces étapes est simplement utilisé comme exemple. Vous devrez le remplacer par votre CLSID unique.

 

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t reg \_ SZ/d "MyCloudStorageApp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>Étape 2 : définir l’image de votre icône

Indiquez le chemin d’accès à l’icône à afficher dans le volet de navigation. Dans l’exemple ci-dessous, *1043* fait référence à l’identificateur de ressource de l’icône dans la dll indiquée.

> [!IMPORTANT]
> Vous devez mettre à jour le chemin d’accès de l’image. Il doit pointer vers un chemin d’accès générique où votre application a installé une image.

 

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon/ve/t reg \_ expand \_ SZ/d%% SystemRoot%% \\ system32 \\imageres.dll,-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Étape 3 : ajouter votre extension au volet de navigation et la rendre visible

L’affectation de la valeur 0x1 indique que l’extension doit être épinglée. Cela permet de s’assurer que les utilisateurs sont affichés par défaut. La configuration par défaut d’un utilisateur est que seuls les éléments épinglés sont affichés dans le volet de navigation. Un utilisateur peut modifier ce paramètre en cliquant avec le bouton droit dans le volet de navigation et en sélectionnant **Afficher tous les dossiers**. Si vous ne souhaitez pas épingler votre extension, vous pouvez définir cette valeur sur 0x0. Cela ne supprime pas votre extension, mais ne l’empêche pas d’être affichée par défaut à l’utilisateur.

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/v System. IsPinnedToNameSpaceTree/t reg \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Étape 4 : définir l’emplacement de votre extension dans le volet de navigation

Cela est essentiel pour s’assurer que le volet de navigation offre une expérience cohérente à l’utilisateur.

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/V SortOrderIndex/t reg \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Étape 5 : fournissez la dll qui héberge votre extension.

Utilisez la shell32.dll pour émuler les dossiers Windows par défaut. Ne modifiez cette valeur que si vous avez une raison particulière de le faire et si vous êtes familiarisé avec les extensions d’espace de noms.

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InprocServer32/ve/t reg \_ expand \_ SZ/d%% SystemRoot%% \\ system32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>Étape 6 : définition de l’objet d’instance

Indiquez que votre extension d’espace de noms doit fonctionner comme d’autres structures de dossiers de fichiers dans l’Explorateur de fichiers. Pour plus d’informations sur les objets d’instance de Shell, consultez [création d’extensions de Shell avec des objets d’instance de Shell](/previous-versions/ms997573(v=msdn.10)).

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instance/v CLSID/T reg \_ SZ/d {0E5AAE11-A475-4c5b-AB00-C66DE400274E}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Étape 7 : fournir les attributs du système de fichiers du dossier cible

Cela est nécessaire pour s’assurer que l’Explorateur de fichiers offre une expérience cohérente et attendue aux utilisateurs. Cette commande définit **le \_ \_ Répertoire des attributs de fichier** et l’attribut de **fichier \_ \_ ReadOnly**, qui sont tous deux des [**constantes d’attribut de fichier**](../fileio/file-attribute-constants.md).

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instance \\ InitPropertyBag/v attributs/t reg \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Étape 8 : définir le chemin d’accès pour la racine de synchronisation

Définissez le chemin d’accès pour la racine de synchronisation.

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ instance \\ InitPropertyBag/v TargetFolderPath/t reg \_ expand \_ SZ/d%% UserProfile%% \\ MyCloudStorageApp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>Étape 9 : définir les indicateurs d’interpréteur de commandes appropriés

Définissez certains indicateurs nécessaires à l’épinglage de votre extension d’espace de noms dans l’arborescence de l’Explorateur de fichiers.

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v FolderValueFlags/t reg \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Étape 10 : définir les indicateurs appropriés pour contrôler votre comportement de l’interpréteur de commandes

Définissez les indicateurs [**SFGAO**](sfgao.md) appropriés. Les indicateurs appropriés sont SFGAO \_ CANCOPY, SFGAO \_ CANLink, SFGAO \_ Storage, SFGAO HASPROPSHEET \_ , SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ Folder, SFGAO \_ FileSystem et SFGAO HASSUBFOLDER \_ .

**Reg Add HKCU \\ Software \\ classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder/v attributs/t reg \_ DWORD/d 0xF080004D/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Étape 11 : inscrire votre extension dans la racine de l’espace de noms

Configurez l’extension d’espace de noms en tant qu’enfant du dossier Desktop.

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/ve/t REG \_ SZ/d MyCloudStorageApp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Étape 12 : masquer votre extension sur le Bureau

Il est important que votre extension apparaisse uniquement dans le volet de navigation de l’Explorateur de fichiers. Une extension d’espace de noms ne fonctionne pas comme un raccourci normal. Par conséquent, vous ne devez pas utiliser cette méthode pour créer un raccourci sur le bureau.

**reg add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ HideDesktopIcons \\ NewStartPanel/v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3}/t REG \_ DWORD/d 0x1/f**

 

 
