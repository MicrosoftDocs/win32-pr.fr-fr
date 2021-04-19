---
title: Explorateur de jeux Windows pour les développeurs de jeux
description: Cet article décrit le processus d’inscription d’un jeu avec l’Explorateur de jeux et les contrôles parents sur Windows Vista et Windows 7 en utilisant le nouveau schéma GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f59b90a23f407be3990a6a4e24b92d39e66852
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513536"
---
# <a name="windows-games-explorer-for-game-developers"></a>Explorateur de jeux Windows pour les développeurs de jeux

Windows Vista améliore l’expérience utilisateur des jeux sur Windows en incluant l’Explorateur de jeux. L’Explorateur de jeux est exposé dans le menu Démarrer de Windows Vista en tant que dossier Games et fournit un emplacement central pour accéder aux jeux.

À partir de la version de mars 2009 du kit de développement logiciel (SDK) DirectX, un nouveau schéma de fichier de définition de jeu (GDF) est utilisé pour prendre en charge les fonctionnalités de Windows 7, du fournisseur de jeux et du flux RSS, et IGameExplorer2. IGameExplorer2 est une nouvelle interface de Windows 7 qui simplifie le processus d’intégration d’un jeu avec l’Explorateur de jeux.

Cet article décrit le processus d’inscription d’un jeu avec l’Explorateur de jeux et les contrôles parents sur Windows Vista et Windows 7 en utilisant le nouveau schéma GDF.

Contenu :

-   [Conditions préalables](#prerequisites)
-   [Intégration à un programme d’installation](#integrating-with-an-installer)
-   [Processus d’intégration](#integration-process)
-   [Tâches de l’Explorateur de jeux](#games-explorer-tasks)
-   [Intégration dans InstallScript](#integrating-into-installscript)
-   [Intégration dans un package MSI](#integrating-into-an-msi-package)
-   [Conseils de débogage](#debugging-tips)
    -   [Tester avec l’exemple de code](#test-with-sample-code)
    -   [Assurez-vous que votre jeu a été correctement supprimé](#make-sure-that-your-game-was-removed-properly)
    -   [Veillez à signer à l’aide d’Authenticode](#be-sure-to-sign-using-authenticode)
    -   [Assurez-vous que les contrôles parentaux sont disponibles](#be-sure-that-parental-controls-are-available)
    -   [Vérifier que les tâches sont de type correct](#verify-that-tasks-are-of-the-correct-type)
    -   [Vérifier les données dans le fichier binaire GDF](#verify-the-data-in-gdf-binary)
-   [Résumé](#summary)

## <a name="prerequisites"></a>Prérequis

Avant de pouvoir intégrer un jeu dans l’Explorateur de jeux, vous devez créer un fichier de définition de jeu (GDF). Une GDF est un fichier XML qui contient des métadonnées décrivant le jeu. Dans la version de mars 2009 du kit de développement logiciel (SDK) DirectX, une section pour le fournisseur de jeux, le flux RSS et la tâche de jeu a été ajoutée au schéma GDF. Pour suivre les instructions de cet article, vous devez utiliser ce nouveau format GDF pour créer votre fichier GDF.

Microsoft fournit un outil de création de GDFs dans le kit de développement logiciel (SDK) DirectX, éditeur de fichiers de définition de jeu, pour faciliter ce processus de création. Cet outil vous permet également de créer des versions localisées d’un GDF.

Une fois qu’un GDF a été créé et localisé, il doit être encapsulé dans une section de ressources d’un fichier binaire (exécutable ou DLL), avec la miniature et l’icône du jeu. GDF contient toutes les métadonnées associées au jeu, y compris l’évaluation du jeu. Le contrôle parental Windows utilise l’évaluation du jeu pour permettre aux parents de contrôler l’accès au jeu. Le fichier binaire qui contient le GDF doit être signé numériquement avec un certificat Authenticode valide. dans le cas contraire, l’Explorateur de jeux et le système de contrôle parental ignorent l’évaluation du jeu, car les informations d’évaluation ne peuvent pas être approuvées sans certification. Pour plus d’informations sur la signature de code avec Authenticode, consultez [signature Authenticode pour les développeurs de jeux](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Intégration à un programme d’installation

Pour simplifier l’intégration de l’Explorateur de jeux, l’exemple GameUXInstallHelper fournit une API commune qui peut être appelée sur Windows XP, Windows Vista et Windows 7. Il est conçu pour utiliser des scripts pour InstallShield et le système d’installation Wise, ainsi que des actions personnalisées MSI et des outils d’installation personnalisés. La détection du système d’exploitation est gérée à l’intérieur de cet exemple de DLL. par conséquent, l’appelant n’a pas à se préoccuper de savoir si le client exécute Windows XP, Windows Vista ou Windows 7.

Les fonctions exportées par cette DLL sont les suivantes :

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Inscrit un jeu avec l’Explorateur de jeux, en fonction d’un chemin d’accès au fichier binaire GDF, un chemin d’accès complet au dossier où le jeu est installé et l’étendue de l’installation.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Inscrit un jeu avec l’Explorateur de jeux ; Version ANSI de **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Supprime un jeu de l’inscription avec l’Explorateur de jeux, en fonction d’un chemin d’accès au fichier binaire GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Supprime un jeu de l’inscription avec l’Explorateur de jeux ; Version ANSI de **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configure les propriétés CustomActionData pour les actions d’une installation personnalisée dépendante MSI. L’utilisation de cette fonction est décrite en détail plus loin dans cet article.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Ajoute un jeu à l’Explorateur de jeux ; à utiliser lors de l’installation d’une action personnalisée MSI.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Supprimer un jeu de l’Explorateur de jeux ; à utiliser lors de l’installation d’une action personnalisée MSI.

</dd> </dl>

Ces fonctions sont expliquées plus en détail dans l’en-tête GameUXInstallHelper. h.

## <a name="integration-process"></a>Processus d’intégration

Une fois que le GDF et les fichiers associés ont été ajoutés à une ressource binaire, il est alors possible d’intégrer le jeu à l’Explorateur de jeux. L’utilisation de **GameUXInstallHelper** simplifie le processus d’intégration. Pour inscrire le jeu avec l’Explorateur de jeux, appelez **GameExplorerInstall** avec un chemin d’accès au fichier binaire GDF, un chemin d’accès complet au dossier où le jeu est installé et l’étendue de l’installation. Pour supprimer l’inscription du jeu, appelez **GameExplorerUninstall** avec un chemin d’accès au fichier binaire GDF.

Notez que le processus de suppression ne supprime qu’une seule installation unique. Si un jeu a été installé plusieurs fois, ce processus doit être répété pour chaque installation unique.

## <a name="games-explorer-tasks"></a>Tâches de l’Explorateur de jeux

Les tâches de l’Explorateur de jeux s’affichent dans le menu contextuel d’un élément dans l’Explorateur de jeux. Les tâches sont réparties entre les tâches de lecture et les tâches de support. Les tâches de lecture lancent un jeu dans un mode particulier, tandis que les tâches de support servent à d’autres fins, y compris la liaison à des sites Web.

Dans Windows Vista, les tâches sont simplement des raccourcis qui se trouvent dans des dossiers spécifiques. Les tâches de lecture et les tâches de support sont stockées dans des dossiers avec les noms correspondants PlayTasks et SupportTasks. GameUXInstallHelper peut lire les informations sur les tâches du jeu à partir du fichier binaire GDF et créer tous les raccourcis automatiquement.

Dans Windows 7, les raccourcis vers les tâches ne sont pas nécessaires, car l’Explorateur de jeux obtient toutes les informations de tâche directement à partir du fichier binaire GDF.

## <a name="integrating-into-installscript"></a>Intégration dans InstallScript

L’appel d’API de l’Explorateur de jeux depuis l’InstallScript d’InstallShield est simplifié à l’aide de l’exemple GameUXInstallHelper. Les étapes requises pour l’intégration à InstallShield sont les suivantes :

1.  Ouvrez un projet InstallScript dans l’éditeur InstallShield.
2.  Ajoutez GameUXInstallHelper.dll au projet à installer dans le répertoire cible.

    **Pour ajouter GameUXInstallHelper.dll à un projet InstallScript :**

    1.  Sous l’onglet **Concepteur d’installation** , cliquez sur données d' **application** dans le volet de navigation de gauche.
    2.  Cliquez sur **fichiers et dossiers** , puis parcourez les **dossiers de l’ordinateur source** pour localiser GameUXInstallerHelper.dll dans les **fichiers de l’ordinateur source**.

        L’emplacement par défaut de GameUXInstallerHelper.dll est DirectX SDK root \\ Samples \\ C++ \\ misc \\ bin \\ x86.

    3.  Sous **dossiers de l’ordinateur de destination**, cliquez sur **dossier cible** de l’application.
    4.  Faites glisser GameUXInstallerHelper.dll des **fichiers de l’ordinateur source** vers les **fichiers de l’ordinateur de destination**.

3.  Dans l’Explorateur InstallScript, cliquez sur le fichier InstallScript (généralement Setup. vie utile restante) qui appelle la fonction DLL.
4.  Collez l’InstallScript suivant dans le fichier :

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>Intégration dans un package MSI

Vous trouverez ci-dessous une description détaillée des étapes requises pour appeler les API de l’Explorateur de jeux à l’aide des actions personnalisées MSI :

1.  Ajoutez une propriété à la table de propriétés MSI nommée « RelativePathToGDF » contenant le chemin d’accès relatif au fichier binaire GDF.
2.  Après l’action CostFinalize, appelez la fonction GameUXInstallHelper DLL **SetMSIGameExplorerProperties** dans une action personnalisée immédiate pour définir les propriétés MSI appropriées pour les autres actions personnalisées.
3.  Lors de l’installation, déclenchez une action personnalisée différée après l’action InstallFiles qui appelle la fonction DLL GameUXInstallHelper **AddToGameExplorerUsingMSI**. Si l’installation est destinée à tous les utilisateurs, l’action personnalisée doit définir l’indicateur msidbCustomActionTypeNoImpersonate ; dans le cas contraire, il ne doit pas définir cet indicateur. Par conséquent, deux actions personnalisées quasiment identiques sont définies : GameUXAddAsAdmin et GameUXAddAsCurUser.
4.  Lors de la suppression de l’installation, déclenchez une action personnalisée différée avant l’action RemoveFiles qui appelle la fonction GameUXInstallHelper DLL **RemoveFromGameExplorerUsingMSI**. Si l’installation a été effectuée pour tous les utilisateurs, l’action personnalisée doit définir l’indicateur msidbCustomActionTypeNoImpersonate ; dans le cas contraire, il ne doit pas définir cet indicateur. Par conséquent, deux actions personnalisées quasiment identiques sont définies : GameUXRemoveAsAdmin et GameUXRemoveAsCurUser.
5.  Définissez des actions personnalisées de restauration pour gérer le cas où l’utilisateur annule l’installation ou la suppression une fois que l’une des actions personnalisées a déjà eu lieu. Il en résulte des 4 actions personnalisées supplémentaires : GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin et GameUXRollBackRemoveAsCurUser.

Cette procédure est décrite en détail dans les instructions suivantes, qui décrivent un processus qui peut être effectué à l’aide d’un éditeur MSI, tel que l’éditeur Orca situé dans le kit de développement logiciel (SDK) de la plateforme. Certains éditeurs MSI possèdent des assistants qui simplifient certaines de ces étapes de configuration.

**Pour configurer un package MSI pour l’intégration avec l’Explorateur de jeux**

1.  Ouvrez le package MSI dans Orca.
2.  Ajoutez la ligne indiquée dans le tableau suivant à la table **binaire** dans le package MSI. 

    | Nom   | Données                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | chemin d’accès au fichier DLL \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Ce fichier sera incorporé dans le package MSI. vous devez donc effectuer cette étape chaque fois que vous recompilez GameUXInstallHelper.dll.

     

3.  Ajoutez les lignes indiquées dans le tableau suivant à la table **CustomAction** dans le package MSI.

    | Action                        | Type                                                                                                                                                                                                   | Source | Cible                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  Ajoutez les valeurs indiquées pour action, condition et séquence dans le tableau suivant à la table **InstallExecuteSequence** dans le package MSI.

    | Action                        | Condition                      | Séquence | Notes                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | Le numéro de séquence place l’action juste après CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NON installé et ALLUSERS     | 4003     | Cette action personnalisée ne se produit qu’au cours d’une nouvelle installation pour tous les utilisateurs. Le numéro de séquence place l’action après InstallFiles et après les restaurations.                                 |
    | GameUXAddAsCurUser            | NON installé et non ALLUSERS | 4004     | Cette action personnalisée ne se produit qu’au cours d’une nouvelle installation de l’utilisateur actuel. Le numéro de séquence place l’action après InstallFiles et après les restaurations.                     |
    | GameUXRollBackAddAsAdmin      | NON installé et ALLUSERS     | 4001     | Cette action personnalisée se produit uniquement lorsqu’une nouvelle installation de tous les utilisateurs est annulée. Le numéro de séquence place l’action après InstallFiles et avant l’action personnalisée ajouter.             |
    | GameUXRollBackAddAsCurUser    | NON installé et non ALLUSERS | 4002     | Cette action personnalisée se produit uniquement lorsqu’une nouvelle installation de l’utilisateur actuel est annulée. Le numéro de séquence place l’action après InstallFiles et avant l’action personnalisée ajouter. |
    | GameUXRemoveAsAdmin           | SUPPRIMER ~ = "ALL" ET ALLUSERS     | 3452     | Cette action personnalisée se produira uniquement pendant la suppression de tous les utilisateurs. Le numéro de séquence place l’action directement avant RemoveFiles et après les restaurations.                                     |
    | GameUXRemoveAsCurUser         | SUPPRIMER ~ = "ALL" ET NON ALLUSERS | 3453     | Cette action personnalisée se produit uniquement lors de la suppression de l’utilisateur actuel. Le numéro de séquence place l’action directement avant RemoveFiles et après les restaurations.                              |
    | GameUXRollBackRemoveAsAdmin   | SUPPRIMER ~ = "ALL" ET ALLUSERS     | 3450     | Cette action personnalisée se produit uniquement lorsque la suppression de tous les utilisateurs est annulée. Le numéro de séquence place l’action directement avant RemoveFiles et avant l’action personnalisée Remove.              |
    | GameUXRollBackRemoveAsCurUser | SUPPRIMER ~ = "ALL" ET NON ALLUSERS | 3451     | Cette action personnalisée se produit uniquement lorsque la suppression de l’utilisateur actuel est annulée. Le numéro de séquence place l’action directement avant RemoveFiles et avant l’action personnalisée Remove.       |

    

     

5.  Ajoutez la ligne indiquée dans le tableau suivant à la table des propriétés dans le package MSI.

    | Propriété          | Valeur                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | nom de chemin d’accès relatif \\ du fichier binaire qui contient GDF |

    

     

    > [!Note]  
    > L’emplacement spécifié par le chemin d’accès est relatif à l’emplacement spécifié par le chemin d’installation. Par exemple, bin \\GDF.dll.

     

6.  Enregistrez le package MSI.

Pour plus d’informations sur les packages et les Windows Installer MSI, consultez [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Conseils de débogage

Voici quelques conseils pour vous aider à déboguer des problèmes lors de l’appel des API de l’Explorateur de jeux :

### <a name="test-with-sample-code"></a>Tester avec l’exemple de code

La création de l’exemple de solution GameUXInstallHelper créera une GameUXInstallHelper.dll et un GDFInstall.exe. Le GDFInstall.exe est un exemple d’application qui utilise des GameUXInstallHelper.dll. L’exécution de GDFInstall.exe demande si vous souhaitez installer ou supprimer un fichier binaire GDF de l’Explorateur de jeux. Vous pouvez tester votre fichier binaire GDF en le transmettant en tant que premier ARG de ligne de commande à GDFInstall.exe.

Si vous n’avez pas de fichier binaire GDF ou que vous ne parvenez pas à installer, essayez d’utiliser l’exemple GDF dans le kit de développement logiciel (SDK) DirectX. L’exemple GDFExampleBinary se trouve dans le kit de développement logiciel (SDK) DirectX et est simplement une DLL qui contient uniquement un fichier GDF. Le projet GDFMaker est également inclus dans la source. Vous pouvez le créer et le tester à l’aide de GDFInstall.exe. Vous pouvez également comparer son XML à la vôtre pour identifier précisément l’endroit où se trouve le problème.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Assurez-vous que votre jeu a été correctement supprimé

Si le jeu est déjà installé dans l’Explorateur de jeux, les appels suivants à **IGameExplorer :: AddGame** renverront E Fail, vérifiez que \_ votre jeu n’est pas installé avant le test. Cela s’applique également si vous installez le GDF uniquement pour l’utilisateur actuel, puis essayez d’installer le GDF pour tous les utilisateurs. Vous devez d’abord supprimer le jeu des utilisateurs actuels avant que **IGameExplorer :: AddGame** aboutisse.

Si vous exécutez **GDFInstall.exe enum**, l’exemple d’application entrera dans un autre mode qui énumère tous les jeux installés de l’Explorateur de jeux et vous invite à les supprimer. Vous pouvez également parcourir et Rechercher dans le registre dans HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ GameUX pour vous assurer que votre jeu n’est pas installé pour un autre utilisateur sur le système. Toutefois, ne modifiez pas ces paramètres de Registre à d’autres fins, car ils ne sont pas toujours compatibles dans les versions ultérieures du système d’exploitation.

### <a name="be-sure-to-sign-using-authenticode"></a>Veillez à signer à l’aide d’Authenticode

Si vous avez fourni une évaluation, mais que vous ne la voyez pas dans l’Explorateur de jeux, assurez-vous que vous avez utilisé Authenticode pour signer le fichier exécutable ou DLL qui contient l’évaluation. L’Explorateur de jeux ignore les informations de classement dans les fichiers non signés. Pour plus d’informations sur Authenticode, consultez [signature Authenticode pour les développeurs de jeux](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Assurez-vous que les contrôles parentaux sont disponibles

Veillez à tester les contrôles parentaux sur une édition de Windows Vista qui fournit des contrôles de contrôle parental : édition familiale basique, édition familiale Premium ou édition intégrale. Windows Vista Professionnel et Windows Vista entreprise n’offrent pas de contrôle parental. Toutefois, si vous effectuez des tests sur Windows Vista Édition intégrale et que l’ordinateur de test est joint à un domaine, vous devez modifier un paramètre de stratégie de groupe rendre les contrôles de contrôle parental visibles. Pour ce faire, consultez [prise en main avec l’Explorateur de jeux](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Vérifier que les tâches sont de type correct

Si vous avez spécifié des tâches de support qui n’apparaissent pas dans l’Explorateur de jeux, vérifiez qu’il s’agit de liens Web. Toutes les autres tâches de raccourci doivent être créées en tant que tâches de lecture. Les tâches sont décrites plus haut dans cet article dans les tâches de l' [Explorateur de jeux](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Vérifier les données dans le fichier binaire GDF

GDFTrace.exe est un outil disponible dans le kit de développement logiciel (SDK) DirectX. Vous pouvez exécuter GDFTrace.exe sur votre fichier binaire GDF et générer toutes les métadonnées GDF contenues dans le fichier binaire pour chaque langue prise en charge pour une validation rapide. Il affiche également les avertissements concernant les informations manquantes ou obsolètes.

## <a name="summary"></a>Résumé

L’Explorateur de jeux de Windows Vista offre un moyen facile et personnalisable de présenter votre jeu aux utilisateurs de Windows Vista, mais vous devez également inscrire le jeu auprès du système pendant le processus d’installation. L’exemple GameUXInstallHelper simplifie grandement ce processus pour les développeurs.

 

 