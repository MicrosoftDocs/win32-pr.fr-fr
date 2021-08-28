---
title: Contrôle de compte d’utilisateur pour les développeurs de jeux
description: cet article décrit les recommandations et les meilleures pratiques permettant aux développeurs de jeux de travailler efficacement avec la fonctionnalité de sécurité contrôle de compte d’utilisateur (UAC) introduite dans Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb8b6ac31ef13e3ace4d439c82f4708673aeffb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886066"
---
# <a name="user-account-control-for-game-developers"></a>Contrôle de compte d’utilisateur pour les développeurs de jeux

cet article décrit les recommandations et les meilleures pratiques permettant aux développeurs de jeux de travailler efficacement avec la fonctionnalité de sécurité contrôle de compte d’utilisateur (UAC) introduite dans Windows Vista.

-   [Vue d’ensemble du contrôle de compte d’utilisateur](#overview-of-user-account-control)
-   [comptes d’utilisateur dans Windows Vista](#user-accounts-in-windows-vista)
-   [Accès aux fichiers en tant qu’utilisateur standard](#file-access-as-a-standard-user)
-   [Accès au registre en tant qu’utilisateur standard](#registry-access-as-a-standard-user)
-   [Privilege Elevation (élévation des privilèges)](#privilege-elevation)
-   [Implications du contrôle de compte d’utilisateur avec CreateProcess ()](#uac-implications-with-createprocess)
-   [Définition du niveau d’exécution dans le manifeste de l’application](#setting-the-execution-level-in-the-application-manifest)
-   [Incorporation d’un manifeste dans Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilité UAC avec les anciens jeux](#uac-compatibility-with-older-games)
-   [Scénarios et manifestes hérités](#legacy-scenarios-and-manifests)
-   [Conclusion](#conclusion)
-   [En savoir plus](#further-reading)

## <a name="overview-of-user-account-control"></a>Vue d’ensemble du contrôle de compte d’utilisateur

le contrôle de compte d’utilisateur (UAC), introduit dans Windows Vista, est une fonctionnalité de sécurité conçue pour empêcher les attaquants malveillants d’utiliser des faiblesses ou des bogues détectés dans des applications largement utilisées pour modifier le système d’exploitation ou d’autres programmes installés. Pour ce faire, vous devez exécuter la grande majorité des programmes et processus en tant qu’utilisateur standard (également appelé utilisateur limité, utilisateur restreint ou Least-Privileged utilisateur), même si le compte de l’utilisateur actuel dispose d’informations d’identification d’administration. Un processus avec des privilèges d’utilisateur standard a de nombreuses restrictions inhérentes qui l’empêchent d’effectuer des modifications à l’ensemble du système.

Le contrôle de compte d’utilisateur est également responsable de l’élévation des privilèges d’un processus à l’aide d’un schéma d’authentification basé sur des boîtes de dialogue, lancé à l’exécution de certains processus qui sont désignés comme nécessitant des privilèges d’administrateur. L’élévation des privilèges permet aux administrateurs d’exécuter la majorité de leurs applications à un niveau de privilège sécurisé (identique à tout autre utilisateur standard), mais également d’autoriser les processus et les opérations qui requièrent des privilèges d’administrateur. Le contrôle de compte d’utilisateur prend en charge l’authentification par procuration afin qu’un administrateur puisse accorder des privilèges élevés à un programme pendant qu’un utilisateur standard est actuellement connecté au système.

La fonctionnalité UAC est activée par défaut. Bien qu’il soit possible pour un administrateur de désactiver l’UAC à l’ensemble du système, cela a un certain nombre de ramifications négatives. Tout d’abord, cela affaiblit la sécurité de tous les comptes d’administration, car tous les processus seraient exécutés avec des informations d’identification d’administration, même si la plupart des applications n’en ont pas besoin. Si le contrôle de compte d’utilisateur est désactivé, une application utilisateur standard qui expose une vulnérabilité exploitable dans la sécurité peut être utilisée pour voler des informations privées, installer des rootkits ou des logiciels espions, détruire l’intégrité du système ou héberger des attaques Zombie sur d’autres systèmes. Tandis que avec le contrôle de compte d’utilisateur activé, l’exécution de la majorité des logiciels en tant qu’utilisateur standard limite les dommages potentiels à un tel bogue. Deuxièmement, la désactivation du contrôle de compte d’utilisateur désactive la plupart des solutions de contournement pour la compatibilité des applications qui permettent aux véritables utilisateurs standard d’exécuter avec succès un large éventail d’applications. La désactivation du contrôle de compte d’utilisateur ne doit jamais être recommandée comme solution de contournement de compatibilité.

Il est important de noter que les applications doivent s’efforcer d’utiliser uniquement des droits d’utilisateur standard, si possible. Alors que les administrateurs peuvent facilement élever les privilèges d’un processus, l’élévation requiert toujours l’intervention de l’utilisateur et l’accusé de réception chaque fois qu’une application est exécutée, ce qui nécessite des informations d’identification d’administration. Cette élévation doit également être effectuée au moment du démarrage du programme. par conséquent, exiger des informations d’identification d’administration même pour une seule opération nécessite d’exposer le système à un risque plus élevé pour l’ensemble de la durée d’exécution de l’application. Les utilisateurs standard sans pouvoir élever leurs privilèges sont également courants dans les paramètres de la famille et de l’entreprise. « Exécuter en tant qu’administrateur » n’est pas une bonne solution de contournement pour la compatibilité, expose l’utilisateur et le système à un risque de sécurité plus élevé et crée des frustrations pour les utilisateurs dans de nombreuses situations.

> [!Note]  
> la fonctionnalité de contrôle de compte d’utilisateur introduite dans Windows Vista est également présente dans Windows 7. Tandis que l’expérience utilisateur qui utilise les différentes fonctionnalités du système a été améliorée par rapport au contrôle de compte d’utilisateur, l’impact sur les applications est fondamentalement le même. toutes les recommandations Windows Vista de cet article s’appliquent également à Windows 7. pour plus d’informations sur les modifications de l’interface utilisateur UAC pour Windows 7, consultez la page [Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>comptes d’utilisateur dans Windows Vista

Windows Vista classe chaque utilisateur en deux types de comptes d’utilisateur : les administrateurs et les utilisateurs standard.

un compte d’utilisateur standard est semblable à un compte d’utilisateur limité dans Windows XP. comme dans Windows XP, un utilisateur standard ne peut pas écrire dans le dossier Program Files, ne peut pas écrire dans la \_ partie HKEY LOCAL \_ MACHINE du registre et ne peut pas effectuer de tâches qui modifient le système, telles que l’installation d’un pilote en mode noyau ou l’accès aux espaces de processus au niveau du système.

le compte administrateur a été considérablement modifié depuis la sortie de Windows XP. Auparavant, tous les processus lancés par un membre du groupe administrateurs recevaient des privilèges d’administrateur. Si le contrôle de compte d’utilisateur est activé, tous les processus s’exécutent avec des privilèges d’utilisateur standard, sauf s’ils sont spécifiquement élevés par un administrateur. Cette différence rend les comptes du groupe administrateurs plus sécurisés en réduisant le risque de sécurité posé par les bogues potentiels dans la plupart des programmes.

Il est important que toutes les applications, en particulier les jeux, fonctionnent efficacement et de manière responsable lorsqu’elles sont exécutées en tant que processus utilisateur standard. Toutes les opérations qui requièrent des privilèges d’administration doivent être effectuées au moment de l’installation ou par des programmes auxiliaires qui demandent explicitement des informations d’identification d’administration. Bien que l’élévation des privilèges soit assez simple pour un membre du groupe administrateurs, les utilisateurs standard doivent s’en remettre à une personne disposant d’informations d’identification d’administration pour entrer physiquement leur mot de passe pour élever les privilèges. étant donné que les comptes protégés par les contrôles parentaux doivent être des utilisateurs standard, il s’agit d’une situation très courante pour les joueurs qui utilisent Windows Vista.

si votre jeu travaille déjà sur Windows XP avec des comptes d’utilisateurs limités, le passage au contrôle de compte d’utilisateur sur Windows Vista doit être très simple. La plupart de ces applications fonctionneront en l’opération, bien que l’ajout d’un manifeste d’application soit fortement recommandé. (Les manifestes sont décrits plus loin dans cette rubrique dans [définition du niveau d’exécution dans le manifeste de l’application](#setting-the-execution-level-in-the-application-manifest).)

## <a name="file-access-as-a-standard-user"></a>Accès aux fichiers en tant qu’utilisateur standard

L’aspect de votre jeu le plus affecté par les restrictions d’utilisateur standard est l’organisation et l’accessibilité du système de fichiers. Vous ne devez jamais supposer que votre jeu peut écrire des fichiers dans le dossier d’installation de votre jeu. dans Windows Vista, par exemple, les privilèges des utilisateurs doivent être élevés par le système d’exploitation avant qu’une application puisse écrire dans le dossier Program Files. pour éviter cela, vous devez classer vos fichiers de données de jeu par portée et accessibilité, et utiliser la fonction [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) , ainsi que les constantes CSIDL fournies par le shell Windows, pour générer les chemins d’accès aux fichiers appropriés. Les constantes CSIDL correspondent aux dossiers connus dans le système de fichiers que le système d’exploitation utilise et promeut pour partitionner les fichiers globaux et spécifiques à l’utilisateur.

toute tentative de création ou d’écriture d’un fichier ou d’un répertoire sous un dossier qui n’accorde pas d’autorisation d’écriture au processus échouera sous Windows Vista si l’application ne dispose pas de privilèges d’administrateur. Si votre exécutable de jeu 32 bits s’exécute en mode hérité, car il n’a pas déclaré de niveau d’exécution demandé, ses opérations d’écriture aboutissent, mais elles sont soumises à la virtualisation, comme décrit dans la section « compatibilité UAC avec les anciens jeux », plus loin dans cet article.

**Tableau 1. Dossiers connus**



| Nom de CSIDL             | chemin d’accès standard (Windows Vista)                                                   | Droits d’utilisateur standard | Droits d'administrateur | Étendue de l’accès | Description                                                                                                                      | Exemples                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ personnel        | C : \\ utilisateurs \\ nom de l’utilisateur \\ documents                                                | Lecture/écriture           | Lecture/écriture           | Per-User     | Fichiers de jeu spécifiques à l’utilisateur qui sont lus et modifiés et peuvent être manipulés en dehors du contexte du jeu.                          | Captures d’écran. Fichiers de jeu enregistrés avec une association d’extension de fichier. |
| CSIDL \_ local \_ AppData  | C : \\ Users \\ nom d’utilisateur \\ AppData \\ local                                           | Lecture/écriture           | Lecture/écriture           | Per-User     | Fichiers de jeu spécifiques à l’utilisateur qui sont lus et modifiés et sont uniquement utilisés dans le contexte du jeu.                                 | Fichiers du cache de jeu. Configurations de lecteur.                          |
| CSIDL \_ Common \_ AppData | C : \\ ProgramData                                                                | Lecture/écriture si propriétaire  | Lecture/écriture           | Tous les utilisateurs    | Fichiers de jeu qui peuvent être créés par un utilisateur et lus par tous les utilisateurs. L’accès en écriture est accordé uniquement au créateur du fichier (propriétaire). | Profils utilisateur                                                     |
| \_fichiers programme \_ CSIDL  | C : \\ Program Files<br/> ou<br/> C : \\ Program Files (x86) <br/> | Lecture seule            | Lecture/écriture           | Tous les utilisateurs    | Fichiers de jeux statiques écrits par le programme d’installation du jeu qui sont lus par tous les utilisateurs.                                                    | Ressources de jeu, telles que des matériaux et des mailles.                        |



 

Votre jeu est généralement installé dans un dossier sous le dossier représenté par la \_ \_ constante fichiers programmes CSIDL. Toutefois, ce n'est pas toujours le cas. Au lieu de cela, vous devez utiliser un chemin d’accès relatif à partir de votre fichier exécutable lors de la génération de chaînes de chemin d’accès aux fichiers ou répertoires situés sous votre dossier d’installation.

Vous devez également vous abstenir des hypothèses codées en dur sur les chemins d’accès aux dossiers connus. par exemple, sur Windows XP Professional édition 64 bits et Windows Vista x64, le chemin d’accès aux fichiers programme est c : \\ program files (x86) pour les programmes 32 bits et c : \\ program files pour les programmes 64 bits. ces chemins d’accès connus sont modifiés par rapport à Windows XP, et les utilisateurs peuvent reconfigurer l’emplacement d’un grand nombre de ces dossiers et même les localiser sur des lecteurs différents. Par conséquent, utilisez toujours les constantes CSIDL pour éviter les confusions et les problèmes potentiels. Windows le programme d’installation comprend ces emplacements de dossiers connus et déplace les données lors de la mise à niveau du système d’exploitation à partir de Windows XP ; en revanche, l’utilisation d’emplacements non standard ou de chemins d’accès codés en dur peut échouer après une mise à niveau du système d’exploitation.

Une attention particulière doit être accordée aux différences discrètes d’utilisation entre les dossiers spécifiques à l’utilisateur spécifiés par CSIDL \_ Personal et CSIDL \_ local \_ AppData. La pratique recommandée pour la sélection de la constante CSIDL à utiliser pour l’écriture d’un fichier consiste à utiliser le paramètre CSIDL \_ Personal si l’utilisateur doit interagir avec le fichier, par exemple en double-cliquant dessus pour l’ouvrir dans un outil ou une application, et pour utiliser CSIDL \_ local \_ AppData pour d’autres fichiers. Les deux dossiers peuvent être exploités par votre application pour stocker et organiser les fichiers de données spécifiques à l’utilisateur, car il n’existe aucune différence au niveau de leur étendue d’accès ou de leurs privilèges. Veillez à créer des noms de chemin d’accès qui sont suffisamment uniques pour ne pas entrer en conflit avec d’autres applications, mais suffisamment court pour conserver le nombre de caractères dans le chemin d’accès complet inférieur à la valeur du \_ chemin d’accès maximal, 260.

Le code suivant fournit un exemple d’écriture d’un fichier dans un dossier connu :

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>Accès au registre en tant qu’utilisateur standard

L’accès au registre par un utilisateur standard est limité de la même façon que le système de fichiers. Un utilisateur standard est autorisé à accéder en lecture à toutes les clés dans le registre ; Toutefois, l’accès en écriture est accordé uniquement à \_ la \_ sous-arborescence HKEY CURRENT USER (HKCU), qui est mappée en interne à la sous-clé spécifique à l’utilisateur HKEY \_ Users \\ ID de sécurité (SID) de l’utilisateur actuel. Une application qui doit écrire dans n’importe quel emplacement du Registre autre que HKEY \_ Current \_ User requiert des privilèges d’administrateur.

Si l’application 32 bits ne contient pas de niveau d’exécution demandé dans son manifeste, toutes les écritures dans HKEY \_ local \_ machine \\ Software sont virtualisées, alors que les écritures dans d’autres emplacements en dehors de HKEY \_ Current \_ User échouent.

Le stockage de données persistantes dans le registre, comme la configuration d’un utilisateur, n’est pas recommandé. La méthode recommandée pour le stockage des données persistantes à partir de votre jeu consiste à écrire les données dans le système de fichiers en appelant [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) et à obtenir la valeur d’une constante CSIDL, décrite dans la section précédente.

## <a name="privilege-elevation"></a>Privilege Elevation (élévation des privilèges)

dans Windows Vista, toute application qui requiert des privilèges d’administrateur doit déclarer une demande de niveau d’exécution administratif dans son manifeste (décrit dans la section suivante, [définition du niveau d’exécution dans le manifeste de l’application](#setting-the-execution-level-in-the-application-manifest)).

L’élévation, telle qu’elle est connue, est la procédure pilotée par UAC pour promouvoir un processus en processus d’administration. Les privilèges d’un processus ne peuvent être élevés qu’au moment de la création. Une fois créé, un processus n’est jamais promu à un niveau de privilège supérieur. Pour cette raison. les opérations qui requièrent des informations d’identification d’administration doivent être isolées dans des programmes d’installation distincts et d’autres programmes auxiliaires.

Lors de l’exécution d’un programme, le contrôle de compte d’utilisateur inspecte le niveau d’exécution demandé dans le manifeste et, si des privilèges élevés sont requis, invite l’utilisateur actuel à l’une des deux boîtes de dialogue standard : l’une pour un utilisateur standard et l’autre pour un administrateur.

Si l’utilisateur actuel est un utilisateur standard, le contrôle de compte d’utilisateur invite l’utilisateur à fournir les informations d’identification d’un administrateur avant d’autoriser l’exécution du programme.

**Figure 1. Demander à un utilisateur standard d’entrer les informations d’identification d’un compte d’administration**

![demander à un utilisateur standard d’entrer les informations d’identification d’un compte d’administration](images/uac-prompt-elevation.jpg)

Si l’utilisateur actuel est un administrateur, le contrôle de compte d’utilisateur demande l’autorisation à l’utilisateur avant d’autoriser son exécution.

**Figure 2. Demander à un administrateur d’autoriser les modifications apportées à l’ordinateur**

![demander à un administrateur d’autoriser les modifications apportées à l’ordinateur](images/uac-prompt-authorization.jpg)

L’application reçoit uniquement des privilèges d’administrateur si un utilisateur standard fournit les informations d’identification d’administration appropriées ou si un utilisateur administratif fournit un accusé de réception. tout autre résultat entraîne l’arrêt de l’application.

Il est important de noter qu’un processus avec des privilèges élevés s’exécute en tant qu’utilisateur administratif qui a entré les informations d’identification dans l’invite UAC plutôt qu’en tant qu’utilisateur standard actuellement connecté. cela est similaire à **RunAs** dans Windows XP le processus avec élévation de privilèges obtient le dossier et les clés de registre de l’administrateur lors de l’accès aux données par utilisateur, et tous les programmes lancés par le processus avec élévation de privilèges héritent également des droits d’administration et des emplacements de compte d’utilisateur. Pour les administrateurs qui sont invités à accepter un accusé de réception (**Continuer** ou **Annuler**), ces emplacements correspondent aux emplacements de l’utilisateur actuel. En général, toutefois, les processus qui nécessitent une élévation ne doivent pas fonctionner sur les données par utilisateur. Notez que cela peut avoir un impact considérable sur la façon dont votre programme d’installation doit fonctionner. Si le programme d’installation, exécuté en tant qu’administrateur, écrit dans HKCU ou dans le profil d’un utilisateur, il peut très bien écrire dans un emplacement incorrect. Envisagez de créer ces valeurs par utilisateur lors de la première exécution du jeu.

## <a name="uac-implications-with-createprocess"></a>Implications du contrôle de compte d’utilisateur avec CreateProcess ()

Le mécanisme d’élévation du contrôle de compte d’utilisateur ne sera pas appelé à partir d’un appel à la fonction Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() pour démarrer un exécutable configuré pour exiger un niveau d’exécution plus élevé que le processus actuel. Par conséquent, l’appel à **CreateProcess**() échouera avec [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() qui retournerait l’élévation d’erreurs \_ \_ requise. **CreateProcess**() ne fonctionnera que si le niveau d’exécution de l’appelé est égal à ou inférieur à celui de l’appelant. Un processus non élevé qui doit générer des processus élevés doit le faire à l’aide de la fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), ce qui entraîne le déclenchement du mécanisme d’élévation du contrôle de compte d’utilisateur au moyen de l’interpréteur de commandes.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Définition du niveau d’exécution dans le manifeste de l’application

Vous déclarez le niveau d’exécution demandé de votre jeu en ajoutant une extension au manifeste de l’application. Le code XML suivant montre la configuration minimale requise pour définir le niveau d’exécution d’une application :

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

Dans le code précédent, le système d’exploitation est informé que le jeu nécessite uniquement des privilèges d’utilisateur standard à l’aide de la balise suivante :

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

En affectant explicitement à requestedExecutionLevel la valeur « asInvoker », cet exemple déclare au système d’exploitation que le jeu se comportera correctement sans privilèges administratifs. par conséquent, le contrôle de compte d’utilisateur désactive la virtualisation et exécute le jeu avec les mêmes privilèges que le demandeur, qui est généralement des privilèges utilisateur standard, puisque l’explorateur de Windows s’exécute en tant qu’utilisateur standard.

Le système d’exploitation peut être informé qu’un jeu requiert une élévation aux privilèges d’administrateur en remplaçant « asInvoker » par « requireAdministrator » pour créer la balise suivante :

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Avec cette configuration, le système d’exploitation invite l’utilisateur actuel à utiliser l’une des boîtes de dialogue d’élévation du contrôle de compte d’utilisateur standard chaque fois que le jeu est exécuté. Il est fortement recommandé qu’aucun jeu ne requière des privilèges d’administrateur pour s’exécuter, car non seulement cette boîte de dialogue devient rapidement gênante, mais elle rend également le jeu incompatible avec les contrôles parentaux. Réfléchissez soigneusement avant d’ajouter cette exigence à n’importe quel exécutable.

Une idée fausse courante est que l’ajout d’un manifeste qui affecte à requestedExecutionLevel la valeur « requireAdministrator » ignore la nécessité d’une invite d’élévation. Ce n’est pas vrai. Cela évite simplement au système d’exploitation de deviner si votre application de mise à jour ou de configuration a besoin de privilèges d’administrateur. L’utilisateur est toujours invité à autoriser l’élévation.

Windows vérifie la signature d’une application marquée pour l’élévation avant d’afficher l’invite UAC. Un exécutable volumineux marqué pour l’élévation prend plus de temps que le nombre de petits exécutables et plus long qu’un exécutable marqué comme « asInvoker ». Les exécutables d’installation qui sont à extraction automatique doivent, par conséquent, être marqués comme « asInvoker » et toute partie qui doit être marquée comme « requireAdministrator » doit être placée dans un exécutable d’assistance séparé.

L’attribut uiAccess, présenté dans les exemples précédents, doit toujours avoir la valeur FALSe pour les jeux. Cet attribut spécifie si les clients UI Automation ont accès à l’interface utilisateur du système protégé et qu’ils ont des implications spéciales en matière de sécurité si la valeur est TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Incorporation d’un manifeste dans Visual Studio

la prise en charge du manifeste a été ajoutée pour la première fois à Visual Studio à partir d’VS2005. par défaut, un fichier exécutable intégré à Visual Studio 2005 (ou plus récent) aura un manifeste généré automatiquement incorporé dans le cadre du processus de génération. Le contenu du manifeste généré automatiquement dépend de certaines configurations de projet que vous spécifiez dans la boîte de dialogue Propriétés du projet.

le manifeste généré automatiquement par Visual Studio 2005 ne contient pas de &lt; &gt; bloc trustInfo, car il n’existe aucun moyen de configurer le niveau d’exécution du contrôle de compte d’utilisateur dans les propriétés du projet. La meilleure façon d’ajouter ces informations est de laisser VS2005 fusionner un manifeste défini par l’utilisateur contenant le &lt; &gt; bloc TrustInfo avec le manifeste généré automatiquement. C’est aussi simple que d’ajouter un \* fichier. manifest à votre solution qui contient le code XML mentionné dans la section précédente. quand Visual Studio rencontre un fichier. manifest dans votre solution, il appelle automatiquement l’outil manifeste (mt.exe) pour fusionner les fichiers. manifest avec l’objet généré automatiquement.

> [!Note]  
> il existe un bogue dans l’outil manifest (mt.exe) fourni par Visual Studio 2005 qui produit un manifeste fusionné et incorporé qui peut provoquer des problèmes lorsque l’exécutable est exécuté sur Windows XP avant SP3. Le bogue est dû à la manière dont l’outil redéfinit l’espace de noms par défaut lors de la déclaration du &lt; &gt; bloc TrustInfo. Heureusement, il est facile de contourner le problème en déclarant explicitement un espace de noms différent dans &lt; le &gt; bloc TrustInfo et en établissant une portée des nœuds enfants sur le nouvel espace de noms. Le code XML fourni dans la section précédente illustre ce correctif.

 

l’un des inconvénients de l’utilisation de l’outil mt.exe inclus dans Visual Studio 2005 est qu’il génère un avertissement lors du traitement du &lt; &gt; bloc trustInfo, car l’outil ne contient pas de schéma mis à jour pour valider le code XML. pour remédier à cet avertissement, il est recommandé de remplacer tous les fichiers mt.exe dans le répertoire d’installation Visual Studio 2005 (il existe plusieurs instances) avec le mt.exe fourni dans le SDK Windows le plus récent.

à compter de Visual Studio 2008, vous pouvez maintenant spécifier le niveau d’exécution d’une application à partir de la boîte de dialogue des propriétés du projet (Figure 3) ou à l’aide de l’indicateur de l’éditeur de liens/manifestuac. la définition de ces options permet à Visual Studio 2008 de générer automatiquement et d’incorporer un manifeste avec le &lt; bloc trustInfo approprié &gt; dans l’exécutable.

**Figure 3. définition du niveau d’exécution dans Visual Studio 2008**

![définition du niveau d’exécution dans Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

l’incorporation d’un manifeste dans les anciennes versions de Visual Studio sans prise en charge du manifeste est toujours possible, mais nécessite davantage de travail du développeur. pour obtenir un exemple sur la façon de procéder, consultez le projet Visual Studio 2003 inclus dans un exemple du kit de développement logiciel (SDK) DirectX antérieur à la version de mars 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilité UAC avec les anciens jeux

si votre jeu semble enregistrer et charger correctement un fichier dans le répertoire Program Files, mais pas de preuve du fichier iOn Windows Vista, toute application 32 bits qui ne contient pas de niveau d’exécution demandé dans son manifeste est considérée comme une application héritée. avant Windows Vista, la plupart des applications étaient généralement exécutées par des utilisateurs disposant de privilèges d’administration. par conséquent, ces applications pouvaient lire et écrire librement des fichiers système et des clés de registre, et de nombreux développeurs n’ont pas effectué les modifications nécessaires pour fonctionner correctement sur les comptes d’utilisateurs limités sur Windows XP. toutefois, sur Windows Vista, ces mêmes applications échouent désormais en raison de privilèges d’accès insuffisants dans le nouveau modèle de sécurité, qui applique l’exécution d’utilisateur standard pour les applications héritées. pour atténuer l’impact de cela, la virtualisation a également été ajoutée à Windows Vista. la virtualisation conservera des milliers d’applications héritées qui fonctionnent bien sur Windows Vista sans que ces applications aient besoin de privilèges élevés à tout moment, simplement pour mener à bien quelques opérations mineures. s trouvés, votre jeu est probablement exécuté en mode hérité et a été soumis à la virtualisation.

La virtualisation affecte le système de fichiers et le registre en redirigeant les écritures sensibles au système (et les opérations de fichier ou de Registre suivantes) vers un emplacement par utilisateur dans le profil de l’utilisateur actuel. Par exemple, si une application tente d’écrire dans le fichier suivant :

<dl> C : \\ Program Files \\ nom de la société \\ titre \\config.ini  
</dl>

l’écriture est automatiquement redirigée vers :

<dl> C : \\ Users \\ nom d’utilisateur \\ AppData \\ local \\ VirtualStore \\ Program Files nom de la \\ société \\ titre \\config.ini  
</dl>

De même, si une application tente d’écrire une valeur de Registre comme suit :

<dl> HKEY \_ local \_ machine \\ Software \\ Company Name \\  
</dl>

elle est redirigée au lieu de :

<dl> HKEY \_ Current \_ User, \\ classes de logiciels \\ \\ VirtualStore \\ machine \\ Software \\ nom \\ de l’entreprise  
</dl>

Les fichiers et les clés de Registre affectés par la virtualisation sont accessibles uniquement par les opérations de fichier et de Registre à partir d’applications virtualisées qui s’exécutent en tant qu’utilisateur actuel.

Toutefois, il existe de nombreuses restrictions à la virtualisation. L’une est que les applications 64 bits ne sont jamais exécutées en mode hérité pour les opérations de compatibilité soumises à la virtualisation dans les applications 32 bits échouent simplement en 64 bits. De même, si une application héritée s’exécutant en tant qu’utilisateur standard tente d’écrire n’importe quel type de fichier exécutable dans un emplacement qui nécessite des informations d’identification d’administration, la virtualisation ne se produit pas et l’écriture échoue.

**Figure 4. Processus de virtualisation**

![processus de virtualisation](images/uac-virtualization-process.jpg)

Lorsqu’une application héritée tente une opération de lecture sur des emplacements sensibles au système dans le système de fichiers ou le registre, les emplacements virtuels sont recherchés en premier. Si le fichier ou la clé de Registre est introuvable, le système d’exploitation accède aux emplacements système par défaut.

la virtualisation sera supprimée des versions ultérieures de Windows donc il est important de ne pas s’appuyer sur cette fonctionnalité. Au lieu de cela, vous devez configurer explicitement votre manifeste d’application pour les privilèges d’administrateur ou d’utilisateur standard, car cela désactive la virtualisation. La virtualisation n’est pas non plus évidente pour les utilisateurs finaux. ainsi, même si la virtualisation peut permettre à votre application de s’exécuter, elle peut générer des appels de support et compliquer la résolution des problèmes pour ces clients.

Notez que si le contrôle de compte d’utilisateur est désactivé, la virtualisation est également désactivée. si la virtualisation est désactivée, les comptes d’utilisateur standard se comportent exactement comme des comptes d’utilisateurs limités dans Windows XP, et les applications héritées peuvent ne pas fonctionner correctement pour les utilisateurs standard qui auraient pu aboutir à cause de la virtualisation.

## <a name="legacy-scenarios-and-manifests"></a>Scénarios et manifestes hérités

Pour la majorité des scénarios d’utilisation, le simple marquage du .exe avec les éléments de manifeste UAC corrects et la garantie que l’application fonctionne correctement comme un utilisateur standard est suffisant pour une excellente compatibilité avec le contrôle de compte d’utilisateur. la plupart des joueurs exécutent Windows Vista ou Windows 7 avec le contrôle de compte d’utilisateur activé. pour les utilisateurs de Windows XP et de Windows Vista ou de la fonctionnalité de contrôle de compte d’utilisateur désactivés, ils s’exécutent généralement à l’aide de comptes d’administrateur. Bien qu’il s’agisse d’un mode de fonctionnement moins sécurisé, il ne s’exécute généralement pas dans des problèmes de compatibilité supplémentaires, mais comme indiqué ci-dessus, la désactivation du contrôle de compte d’utilisateur désactive également la virtualisation.

Il existe un cas particulier à noter lorsque le programme est marqué comme « requireAdministrator » dans le manifeste de contrôle de compte d’utilisateur. sur Windows XP et sur Windows Vista ou Windows 7 avec le contrôle de compte d’utilisateur désactivé, les éléments du manifeste UAC sont ignorés par le système. Dans ce cas, les utilisateurs disposant de comptes d’administrateur exécuteront toujours tous les programmes avec des droits d’administrateur complets, et ces programmes fonctionneront donc comme prévu. Windows XP les utilisateurs limités et les utilisateurs Standard s’exécutant sur Windows Vista ou Windows 7, toutefois, exécutent toujours ces programmes avec des droits restreints et toutes les opérations de niveau administrateur échouent. Par conséquent, il est recommandé que les programmes marqués comme « requiretAdministrator » appellent [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) au démarrage et affichent un message d’erreur irrécupérable s’ils retournent la valeur false. Pour la majorité des scénarios ci-dessus, cette opération est toujours réussie, mais offre une meilleure expérience utilisateur et un message d’erreur clair pour cette situation rare.

## <a name="conclusion"></a>Conclusion

en tant que développeur de jeux ciblant le Windows environnement multi-utilisateur, il est impératif que vous conceviez votre jeu pour qu’il fonctionne de manière efficace et responsable. Le fichier exécutable principal de votre jeu ne doit pas dépendre des privilèges d’administrateur. Cela empêche non seulement l’apparition d’invites d’élévation chaque fois que votre jeu est exécuté, ce qui peut avoir un impact négatif sur l’expérience globale de l’utilisateur, mais il permet également à votre jeu de tirer parti d’autres fonctionnalités qui nécessitent une exécution avec des privilèges d’utilisateur standard, tels que les contrôles de contrôle parental.

les Applications qui sont correctement conçues pour fonctionner comme avec les informations d’identification d’un utilisateur standard (ou utilisateur limité) dans les versions précédentes de Windows ne seront pas affectées par l’UAC qu’elles s’exécuteront sans élévation. Toutefois, ils doivent inclure un manifeste dont le niveau d’exécution demandé est défini sur « asInvoker » pour se conformer aux normes d’application pour Vista.

## <a name="further-reading"></a>En savoir plus

pour obtenir de l’aide sur la conception d’applications pour Windows Vista conformes au contrôle de compte d’utilisateur, téléchargez le livre blanc suivant : [Windows vista Application Development requirements for user account control compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

Ce livre blanc fournit des étapes détaillées sur le processus de conception, ainsi que des exemples de code, des exigences et des meilleures pratiques. ce document décrit également les mises à jour techniques et les modifications apportées à l’expérience utilisateur dans Windows Vista.

pour plus d’informations sur le contrôle de compte d’utilisateur, consultez [Windows Vista : contrôle de compte d’utilisateur](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) sur [Microsoft TechNet](https://www.microsoft.com/technet/).

une autre ressource utile est l’article [apprendre à vos applications à fonctionner avec le contrôle de compte d’utilisateur Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control), du [Magazine MSDN](/archive/msdn-magazine/msdn-magazine-issues), du 2007 janvier. cet article décrit les problèmes généraux de compatibilité des applications, ainsi que les avantages et les problèmes liés à l’utilisation de packages Windows Installer sur Windows Vista.

pour plus d’informations sur le bogue et le correctif pour mt.exe, l’outil utilisé par Visual Studio 2005 pour fusionner et incorporer automatiquement un manifeste dans un fichier exécutable, consultez [exploration des manifestes partie 2 : espaces de noms par défaut et manifestes de contrôle de compte d’utilisateur de Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) sur le blog de Chris Jackson sur [MSDN](/archive/blogs/).

 

