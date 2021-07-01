---
title: Pare-feu Windows pour les développeurs de jeux
description: 'Cet article décrit le pare-feu Windows : pourquoi il existe, ce qu’il accomplit et de quelle manière. Plus important encore, il décrit comment configurer votre jeu pour qu’il fonctionne correctement avec le pare-feu.'
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c7ff3c9b651b6264703732f0eec57054784034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120234"
---
# <a name="windows-firewall-for-game-developers"></a>Pare-feu Windows pour les développeurs de jeux

Cet article décrit le pare-feu Windows : pourquoi il existe, ce qu’il accomplit et de quelle manière. Plus important encore, il décrit comment configurer votre jeu pour qu’il fonctionne correctement avec le pare-feu.

Contenu :

-   [Qu’est-ce qu’un pare-feu ?](#what-is-a-firewall)
-   [Comment puis-je savoir si mon jeu est affecté ?](#how-can-i-tell-if-my-game-is-affected)
-   [Le pare-feu avant Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Le pare-feu Windows XP SP2 est plus performant](#windows-xp-sp2-firewall-is-better)
-   [Utilisation du pare-feu Windows](#working-with-the-windows-firewall)
-   [Intégration à l’aide d’InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Intégration à Wise pour Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Intégration dans Windows Installer](#integrating-into-windows-installer)
-   [Recommandations](#recommendations)

## <a name="what-is-a-firewall"></a>Qu’est-ce qu’un pare-feu ?

Le pare-feu offre une barrière contre les intrusions basées sur le réseau. Il bloque le trafic entrant non sollicité et rend le système pratiquement invisible sur Internet en rejetant les demandes ICMP (Internet Control Message Protocol). Cela signifie que les commandes ping et tracert ne fonctionneront pas. Le pare-feu recherche et rejette également les paquets non valides.

Cette barrière empêche les attaques opportunistes. Les attaques se répandent en recherchant de nombreux systèmes avec la même vulnérabilité. Le pare-feu peut contrecarrer de nombreuses attaques en plaçant un signe « ne pas déranger » pour les fonctionnalités qui ne sont pas en cours d’utilisation. l’attaque est ignorée et n’est pas à la racine. L’avantage essentiel du pare-feu Windows est que les fonctionnalités et les applications qui ne sont pas utilisées ne peuvent pas être des brèches pour les attaques.

L’utilisateur configure le système pour identifier les applications et les fonctionnalités nécessaires et doit être ouvert sur le réseau. Cela se produit lorsqu’une application est installée ou lorsqu’elle essaie de s’ouvrir sur le réseau.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Comment puis-je savoir si mon jeu est affecté ?

Avec l’arrivée de Windows XP SP2, le pare-feu Windows a été largement déployé. Tous les jeux Windows multijoueur sont affectés à un certain degré. Alors que les clients sont généralement de forme correcte, les serveurs, les hôtes et les pairs de pair à pair requièrent que le pare-feu soit configuré pour continuer à fonctionner. Plus précisément, le trafic entrant non sollicité est abandonné. Le pare-feu intercepte les paquets de filtre du trafic réseau en fonction du contenu du paquet et de l’activité réseau récente. Le pare-feu utilise le contenu et l’activité pour décider de transférer ou de supprimer un paquet. Une fois le pare-feu correctement configuré, un jeu est en mesure d’accepter le trafic entrant non sollicité comme avant.

Qui a le trafic entrant non sollicité ?

-   Client/serveur : tous les participants se connectent à un serveur central. Le serveur central est celui avec le trafic entrant non sollicité. Les clients qui se connectent au serveur sollicitent le trafic de retour, ce qui est attendu et est autorisé à traverser le pare-feu si les règles pour les clients sont respectées. Le serveur central doit être configuré pour accepter le trafic non sollicité afin d’autoriser le trafic client à traverser le pare-feu.
-   Massivement multijoueur (MMP) : tous les participants sont connectés à un centre de données. Il s’agit d’une relation client/serveur complexe, car le centre de données a le trafic entrant non sollicité. Les participants sont des clients et, en général, n’ont pas besoin d’accepter le trafic non sollicité.
-   Pair à pair, où tous les participants sont connectés directement : tous les participants doivent être prêts à accepter le trafic non sollicité de la part de tout nouveau joueur qui rejoint le groupe. Dans un sens, chacun des participants doit fonctionner comme un hôte, de sorte qu’ils doivent tous être configurés comme s’ils étaient des hôtes.

Les clients sont généralement en bonne forme. Leurs connexions TCP/IP (Transmission Control Protocol/Internet Protocol) sortantes fonctionneront correctement, de même que les messages UDP (User Datagram Protocol) sortants, ainsi que les réponses à ces messages. le pare-feu maintient le port ouvert pendant 90 secondes après chaque message sortant en prévision d’une réponse.

## <a name="the-firewall-before-windows-xp-sp2"></a>Le pare-feu avant Windows XP SP2

Le pare-feu de connexion Internet (ICF) de Windows XP et de Windows Server 2003 est un filtre de paquets avec état, et gère le protocole Internet version 4 (IPv4) et le protocole Internet version 6 (IPv6). Toutefois, il n’est pas activé par défaut et ne prend pas en charge les piles réseau tierces, dont il existe un nombre important dans le monde, tel que les fournisseurs de services Internet importants, y compris les sociétés de téléphone nationales.

Pour ceux qui ne sont pas sur Windows XP SP2, il est fortement recommandé d’activer le pare-feu de connexion Internet. Consultez les instructions « utiliser un pare-feu Internet » lors de https://www.microsoft.com/security/protect la première étape de la sécurisation de votre ordinateur. Le pare-feu de connexion Internet (ICF) fournit un mappage de port pour remplacer le filtre de paquets. Pour l’essentiel, vous spécifiez le port à ouvrir et il reste ouvert jusqu’à ce que vous le fermiez. Si l’utilisateur redémarre avant qu’il ne soit fermé, il restera ouvert jusqu’à ce qu’il soit fermé spécifiquement. Le contrôle du pare-feu et la gestion des mappages de port s’effectuent via [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) et [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Le pare-feu Windows pour Windows XP SP2 est une solution plus complète qui prend en charge les piles réseau tierces, et gère les ports de manière plus intelligente : les ports restent ouverts uniquement tant que l’application qui en a besoin est toujours active.

## <a name="windows-xp-sp2-firewall-is-better"></a>Le pare-feu Windows XP SP2 est plus performant

Windows XP SP2 met hors service les choix et les paramètres de sécurité. L’objectif est de protéger par défaut et de permettre à l’utilisateur de faire des choix informés sur les applications qui sont autorisées à s’exécuter sur leur ordinateur.

Le nouveau pare-feu Windows est disponible sur Windows XP SP2 et Windows Server 2003 Service Pack 1 (SP1). À l’instar de l’ICF, il s’agit d’un pare-feu logiciel qui prend en charge IPv4 et IPv6, mais contrairement à ICF, le pare-feu Windows :

-   Dispose d’une protection du système au moment de l’amorçage, éliminant une petite fenêtre de vulnérabilité au démarrage.
-   Prend en charge les piles réseau tierces.
-   A un mode « activé sans exceptions » qui bloque tous les paquets entrants non sollicités. C’est très utile lorsque vous utilisez un réseau public, par exemple dans un aéroport ou un café.

Dans le mode « activé sans exceptions », tous les trous statiques sont fermés. Les appels d’API permettant d’ouvrir un trou statique sont autorisés mais différés ; autrement dit, elles ne sont pas appliquées tant que le pare-feu n’est pas rétabli en mode de fonctionnement normal. Toutes les demandes Listen émises par les applications seront également ignorées. Les connexions sortantes continuent de fonctionner.

Pour les nouvelles applications, ajoutez votre application à la « liste des exceptions » au cours de l’installation. Vous pouvez ajouter l’application à l’aide de l’interface [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , en fournissant le chemin d’accès complet. Nous allons aborder les détails dans l’exemple.

En guise de note, vous vous demandez peut-être s’il s’agit d’un risque pour la sécurité que les applications peuvent ajouter et supprimer des applications dans la liste des exceptions, quelle que soit l’intervention de l’utilisateur, ou peut-être vous pensez que les applications peuvent désactiver complètement le pare-feu. Pour ce faire, l’application doit disposer de privilèges d’administrateur. Si du code malveillant s’exécute en mode administrateur sur votre système, le jeu est déjà sur et le pirate a déjà gagné. La possibilité pour le pirate de désactiver le pare-feu mériterait un peu plus qu’une note de bas de page.

Les applications héritées, y compris les applications installées avant la mise à niveau de l’utilisateur vers Windows XP SP2, sont gérées avec la liste contextuelle des exceptions (voir figure 1). Cette boîte de dialogue s’affiche lorsqu’une application tente d’ouvrir un port pour le trafic entrant, soit lors de l’appel de bind () avec un port différent de zéro pour UDP, soit avec Accept () pour le protocole TCP/IP. Vous devez être en cours d’exécution en tant qu’administrateur pour débloquer des applications, tandis que « me le demander ultérieurement » n’autorise pas cette opération, mais le demande la prochaine fois.

Il s’agit d’une boîte de dialogue modale non bloquante. Lors de l’exécution d’une application Microsoft Direct3D de plein écran, la boîte de dialogue est disponible en dessous ; l’utilisateur peut alors le gérer lorsque l’application quitte le mode plein écran ou la touche Alt-Tab pour revenir au bureau. Toutefois, il n’est pas toujours évident pour l’utilisateur que cette boîte de dialogue apparaissait lorsqu’un jeu s’exécute en plein écran. il est donc important d’éviter d’afficher cette boîte de dialogue à l’aide de l’interface [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , comme indiqué ci-dessous.

**Figure 1. Boîte de dialogue contextuelle liste des exceptions**

![boîte de dialogue contextuelle liste des exceptions](images/firewalls1.jpg)

Vous remarquerez que la fenêtre contextuelle connaît le nom et l’éditeur de l’application. Il n’y a pas de magie ici : elles sont extraites des informations de version de l’exécutable. Ces informations constituent un outil d’administration de système important. Il est même utilisé pour le travail de compatibilité des applications en continu. Certaines applications négligent de conserver les informations de cette version à jour.

Les utilisateurs peuvent également ajouter leurs applications par le biais de l’interface utilisateur (voir figure 2).

**Figure 2. Configuration du pare-feu**

![configuration du pare-feu](images/firewalls2.jpg)

**Figure 3. Ajout d’un programme à la liste d’exceptions de pare-feu**

![Ajout d’un programme à la liste d’exceptions de pare-feu](images/firewalls3.jpg)

Le meilleur scénario consiste à faire en sorte que les ajouts et les suppressions de la liste d’exceptions soient automatisés. Le meilleur moment pour effectuer ces ajouts et suppressions est pendant le processus d’installation et de désinstallation. L’ajout ou la suppression de la liste d’exceptions de pare-feu nécessite des privilèges d’administrateur. par conséquent, veillez à prendre en compte.

## <a name="working-with-the-windows-firewall"></a>Utilisation du pare-feu Windows

Là encore, la plupart des jeux doivent uniquement être ajoutés à la liste des exceptions du pare-feu s’ils peuvent fonctionner en tant que serveur ou s’ils implémentent un protocole de communication d’égal à égal. Le FirewallInstallHelper.dll est un exemple de DLL qui peut être appelé à partir d’un programme d’installation. La source est fournie si vous souhaitez intégrer directement la source à votre propre application. L’exemple est disponible ici :



|             | Fichier                                                                             |
|-------------|------------------------------------------------------------------------------|
| **Source :**     | (Racine SDK) \\ Exemples \\ \\ FirewallInstallHelper divers \\ C++                        |
| **Exécutable** | (Racine SDK) \\ Exemples \\ de \\ \\ casiers divers C++ \\ <arch> \\FirewallInstallHelper.dll |



 

Les fonctions exportées par cette DLL sont les suivantes :

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Cette fonction ajoute une application à la liste d’exceptions. Il prend un chemin d’accès complet à l’exécutable et un nom convivial qui s’affiche dans la liste des exceptions du pare-feu. Cette fonction requiert des privilèges d’administrateur.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Version ANSI de **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Cette fonction supprime l’application de la liste d’exceptions. Elle prend un chemin d’accès complet à l’exécutable. Cette fonction requiert des privilèges d’administrateur

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Version ANSI de **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Cette fonction signale si l’application a été désactivée ou supprimée de la liste des exceptions. Elle doit être appelée chaque fois que le jeu est exécuté. La fonction prend un chemin d’accès complet à l’exécutable. Cette fonction ne requiert pas de privilèges d’administrateur.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Version ANSI de **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Appelez cette opération uniquement si vous utilisez des actions personnalisées dans Windows Installer. Vous trouverez plus de détails à la suite.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Appelez cette opération uniquement si vous utilisez des actions personnalisées dans Windows Installer. Vous trouverez plus de détails à la suite.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Appelez cette opération uniquement si vous utilisez des actions personnalisées dans Windows Installer. Vous trouverez plus de détails à la suite.

</dd> </dl>

Les sections suivantes décrivent des méthodes spécifiques d’appel des fonctions DLL exportées à partir de ce FirewallInstallHelper à partir d’un package InstallShield, Wise ou Windows Installer. Toutes les méthodes restituent les mêmes résultats et il revient au développeur de déterminer la méthode à implémenter.

## <a name="integrating-using-installshield-installscript"></a>Intégration à l’aide d’InstallShield InstallScript

Une autre méthode d’utilisation des API de pare-feu consiste à ajouter les appels de fonction à un InstallScript InstallShield. Les étapes requises pour l’intégration de sont relativement simples :

1.  Ouvrez un projet InstallScript dans l’éditeur InstallShield.
2.  Ajoutez le FirewallInstallHelper.dll au projet en tant que fichier de support.

    1.  Sous l’onglet Assistant projet, ouvrez l’onglet fichiers d’application.
    2.  Cliquez sur le bouton Ajouter des fichiers pour ajouter des fichiers au dossier cible de l’application.
    3.  Accédez au FirewallInstallHelper.dll que vous avez créé ou utilisez celui fourni dans le kit de développement logiciel (SDK) DirectX et ajoutez-le au projet.

3.  Ajoutez InstallScript au projet.

    1.  Ouvrez la vue du concepteur d’installation, puis cliquez sur le comportement et la logique \| InstallScript
    2.  Cliquez sur le fichier InstallScript (généralement Setup. vie utile restante) pour l’ouvrir dans l’éditeur.
    3.  Collez le code suivant dans le fichier InstallScript :

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  Modifiez les commentaires TODO avec le nom de l’application qui s’affiche dans la liste des exceptions du pare-feu et le chemin d’accès à l’exécutable du jeu relatif au répertoire d’installation.

## <a name="integrating-into-wise-for-windows-installer"></a>Intégration à Wise pour Windows Installer

Pour une intégration avec Wise pour Windows Installer, vous devez effectuer les étapes suivantes :

1.  Ouvrez votre Wise pour Windows Installer projet.
2.  Sélectionnez l’onglet « expert d’installation » en bas.
3.  Cliquez sur fichiers, puis ajoutez le FirewallInstallHelper.dll à partir du DXSDK dans le répertoire d’installation du jeu.
4.  Sélectionnez l’onglet « script MSI » en bas.
5.  Sélectionnez l’onglet « exécuter immédiatement » près du bas.
6.  Après CostFinalize, ajoutez une action « définir la propriété » qui définit FULLPATH sur \[ « \] chemin d’accès relatif du chemin d’accès au fichier exécutable à partir du répertoire d’installation ». Par exemple, « \[ INSTALLDIR \]game.exe » sans les guillemets
7.  Sélectionnez l’onglet « exécuter différé » près du bas.
8.  Après PublishProduct, ajoutez une instruction « if » avec la condition « non installé » (sensible à la casse).
9.  Dans le bloc If, ajoutez une action « appeler une DLL personnalisée à partir de la destination ».

    1.  Définissez le champ fichier DLL sur « \[ INSTALLDIR \]FirewallInstallHelper.dll ».
    2.  Définissez le champ nom de la fonction sur « AddApplicationToExceptionListA ».
    3.  Ajoutez un paramètre avec le type « pointeur de chaîne », la source de valeur « propriété » et le nom de propriété « FULLPATH ».
    4.  Ajoutez un deuxième paramètre avec le type « pointeur de chaîne », source de valeur « constante » et définissez la valeur de constante sur le nom d’application convivial que vous souhaitez afficher dans la liste d’exceptions de pare-feu.
    5.  Fermez le bloc If en ajoutant une instruction « end Statement ».

10. Juste au-dessus de l’action RemoveFiles près du haut, ajoutez un autre bloc If, avec la condition « REMOVE ~ = "ALL » (respect de la casse et sans les guillemets externes).
11. Dans le deuxième bloc If, ajoutez une action « appeler une DLL personnalisée à partir de la destination ».

    1.  Définissez le champ fichier DLL sur « \[ INSTALLDIR \]FirewallInstallHelper.dll ».
    2.  Définissez le champ nom de la fonction sur « RemoveApplicationFromExceptionListA ».
    3.  Ajoutez un paramètre avec le type « pointeur de chaîne », la source de valeur « propriété » et le nom de propriété « FULLPATH ».
    4.  Fermez le deuxième bloc If en ajoutant une instruction « end Statement ».

## <a name="integrating-into-windows-installer"></a>Intégration dans Windows Installer

Pour une intégration avec Windows Installer au niveau supérieur, vous devez effectuer ces étapes. Elles sont expliquées en détail ci-dessous :

-   Ajoutez 2 propriétés « FriendlyNameForFirewall » et « RelativePathToExeForFirewall » comme décrit ci-dessous.
-   Après l’action CostFinalize, appelez « SetMSIFirewallProperties » dans une action personnalisée immédiate pour définir les propriétés MSI appropriées pour les autres actions personnalisées.
-   Pendant l’installation après l’action InstallFiles, appelez une action personnalisée différée qui utilise la fonction « AddToExceptionListUsingMSI » de FirewallInstallHelper.
-   Pendant la désinstallation après l’action InstallFiles, appelez une action personnalisée différée qui utilise la fonction « RemoveFromExceptionListUsingMSI » de FirewallInstallHelper.
-   Pendant la restauration, appelez une action personnalisée différée qui appelle également la fonction « RemoveFromExceptionListUsingMSI » de FirewallInstallHelper.

Vous trouverez ci-dessous les étapes nécessaires pour effectuer cette opération à l’aide d’un éditeur MSI comme Orca dans le kit de développement logiciel (SDK) de plateforme. Notez que certains éditeurs comportent des assistants qui simplifient certaines de ces étapes :

1.  Ouvrez le package MSI dans Orca.
2.  Ajoutez le code suivant à la table binaire :

    

    | Nom     | Données                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | PARE | Pointez sur le FirewallInstallHelper.dll. Ce fichier sera incorporé dans le package MSI. vous devrez donc effectuer cette étape chaque fois que vous recompilez FirewallInstallHelper.dll. |

    

     

3.  Ajoutez le code suivant à la table CustomAction :

    

    | Action                   | Type                                                                                                                                                                                                   | Source   | Cible                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | PARE | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | PARE | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | PARE | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | PARE | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | PARE | AddToExceptionListUsingMSI      |

    

     

4.  Ajoutez le code suivant à la table InstallExecuteSequence :

    

    | Action                   | Condition     | Séquence | Remarques                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Cela place juste après CostFinalize.                                                                                                                                       |
    | FirewallAdd              | NON installé | 4021     | Cette action personnalisée se produit uniquement lors d’une nouvelle installation. Le numéro de séquence place l’action après InstallFiles et après les restaurations.                              |
    | FirewallRollBackAdd      | NON installé | 4020     | Cette action personnalisée se produit uniquement lors de l’annulation d’une nouvelle installation. Le numéro de séquence place l’action après InstallFiles et avant l’action personnalisée ajouter.          |
    | FirewallRemove           | Installé     | 3461     | Cette action personnalisée se produira uniquement pendant la désinstallation. Le numéro de séquence place l’action directement avant RemoveFiles et après les restaurations.                           |
    | FirewallRollBackRemove   | NON installé | 3460     | Cette action personnalisée se produit uniquement lorsqu’une désinstallation est annulée. Le numéro de séquence place l’action directement avant RemoveFiles et avant l’action personnalisée Remove. |

    

     

5.  Ajoutez le code suivant à la table de propriétés :

    

    | Propriété                     | Value                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Doit être le nom que la liste d’exceptions affichera. Par exemple, « exemple de jeu » |
    | RelativePathToExeForFirewall | Doit être l’exécutable installé du jeu. Par exemple, « ExampleGame.exe »  |

    

     

Pour plus d’informations sur la Windows Installer, consultez [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Recommandations

Le pare-feu est ici pour rester en contact. Ces recommandations permettront à vos clients de bénéficier d’une bonne expérience de pare-feu avec votre jeu Windows :

-   N’indiquez pas aux utilisateurs de désactiver le pare-feu pour jouer votre jeu. Cela rend la machine entière vulnérable, même lorsqu’elle ne lit pas votre jeu.
-   Rendez la configuration du pare-feu transparente pour vos utilisateurs. Ajoutez votre application à la liste des exceptions pendant l’installation et supprimez votre application de la liste des exceptions lors de l’installation.
-   Envoyer des commentaires à l’utilisateur si le mode multijoueur est bloqué par l’état du pare-feu. Par exemple, désactivez les fonctionnalités de mise en réseau si elles ne fonctionnent pas, soit parce que l’application n’est pas autorisée, soit parce que le système est en mode « aucune exception ».

 

 