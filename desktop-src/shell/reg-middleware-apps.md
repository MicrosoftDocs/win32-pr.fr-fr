---
description: 'cette rubrique explique comment inscrire un programme dans le registre Windows en tant qu’un des types de client suivants : navigateur, courrier électronique, lecture multimédia, messagerie instantanée ou machine virtuelle pour Java.'
title: Inscription de programmes avec des types de clients
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470417"
---
# <a name="registering-programs-with-client-types"></a>Inscription de programmes avec des types de clients

cette rubrique explique comment inscrire un programme dans le registre Windows en tant qu’un des types de client suivants : navigateur, courrier électronique, lecture multimédia, messagerie instantanée ou machine virtuelle pour Java.

> [!Note]  
> Ces informations s’appliquent aux systèmes d’exploitation suivants :
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

Cette rubrique comprend les sections suivantes.

-   [Éléments d’inscription courants pour tous les types de clients](#common-registration-elements-for-all-client-types)
    -   [Sélection d’un nom canonique](#selecting-a-canonical-name)
    -   [Inscription du nom complet d’un programme](#registering-a-programs-display-name)
    -   [Inscription de l’icône d’un programme](#registering-a-programs-icon)
    -   [Inscription d’un verbe ouvert](#registering-an-open-verb)
    -   [Inscription des informations d’installation](#registering-installation-information)
-   [Éléments d’inscription pour des types de client spécifiques](#registration-elements-for-specific-client-types)
    -   [Enregistrement du menu Démarrer](#start-menu-registration)
    -   [Inscription du client de messagerie](#mail-client-registration)
-   [Compléter les exemples d’inscriptions](#complete-sample-registrations)
    -   [Exemple de navigateur](#a-sample-browser)
    -   [Exemple de navigateur de messagerie](#a-sample-mail-browser)
    -   [Exemple de lecteur multimédia](#a-sample-media-player)
    -   [Exemple de programme Instant Messenger](#a-sample-instant-messenger-program)
    -   [Exemple de machine virtuelle Java](#a-sample-virtual-machine-for-java)
-   [Rubriques connexes](#related-topics)

Cette rubrique étend la documentation existante sur l’inscription d’un programme en tant que type de client particulier. Pour obtenir des liens vers cette documentation, consultez la section Rubriques connexes.

## <a name="common-registration-elements-for-all-client-types"></a>Éléments d’inscription courants pour tous les types de clients

Lors de l’inscription d’un programme en tant que type de client, la plupart des entrées de Registre sont les mêmes, quel que soit le type de client. Certaines entrées du Registre, toutefois, sont spécifiques au type de client et sont indiquées dans la section [éléments d’inscription pour des types de client spécifiques](#registration-elements-for-specific-client-types) .

Cette section aborde les sujets suivants :

-   [Sélection d’un nom canonique](#selecting-a-canonical-name)
-   [Inscription du nom complet d’un programme](#registering-a-programs-display-name)
-   [Inscription de l’icône d’un programme](#registering-a-programs-icon)
-   [Inscription d’un verbe ouvert](#registering-an-open-verb)
-   [Inscription des informations d’installation](#registering-installation-information)

> [!Note]  
> Les noms de sous-clés donnés en italiques dans cette rubrique sont des espaces réservés pour les noms de sous-clés définis par l’utilisateur ou un ensemble de valeurs possibles. Des exemples complets avec des exemples de noms en place sont fournis dans la section [inscriptions des exemples complets](#complete-sample-registrations) .

 

Toutes les informations d’inscription de type client sont stockées sous la sous-clé suivante :

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* est l’un des noms de sous-clés suivants :

-   StartMenuInternet (pour les navigateurs)
-   Courrier électronique (pour courrier électronique)
-   Média (pour la lecture du média)
-   MESSAGERIE instantanée (pour la messagerie instantanée)
-   JavaVM (pour machine virtuelle Java)

Tout au long de cette rubrique, vous allez noter des références à un programme informatique fictif nommé « lit View » par Litware Inc., avec un fichier exécutable nommé Litview.exe. Ce programme hypothétique est utilisé de manière interchangeable comme une messagerie instantanée, un navigateur ou un autre type de programme client si nécessaire à des fins d’illustration.

### <a name="selecting-a-canonical-name"></a>Sélection d’un nom canonique

Le fournisseur doit choisir un *nom canonique* pour le programme. Le nom canonique n’est jamais présenté à l’utilisateur, il n’est donc pas nécessaire de le localiser. Son seul objectif est de fournir une chaîne unique qui peut être utilisée pour identifier le programme. Il est généralement identique au nom anglais du programme, mais il s’agit simplement d’une convention.

Pour les types de clients autres que les navigateurs, le nom canonique peut être n’importe quelle chaîne. Choisissez un nom unique, qui n’est pas susceptible d’être utilisé par un autre fournisseur.

Pour les clients de navigateur, le nom canonique doit être le nom, y compris l’extension, du fichier exécutable associé ; par exemple, « Litview.exe ».

Voici quelques exemples de noms canoniques.

-   Iexplore.exe (navigateur)
-   Windows Courrier électronique (e-mail)
-   Lecteur Windows Media (support)
-   Windows Messenger (messagerie instantanée)

Inscrivez le nom canonique en créant une sous-clé comme indiqué ici. Le nom de la sous-clé est le nom canonique. Toutes les informations relatives à l’inscription de ce programme se trouvent sous cette sous-clé.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Inscription du nom complet d’un programme

L’étape suivante de l’inscription consiste à spécifier le nom d’affichage du programme. Elle est fournie sous la forme d’une valeur sous la clé de nom canonique comme indiqué ici. Notez à nouveau que *CanonicalName* et *ClientTypeName* ne sont pas les noms réels des clés, mais uniquement des espaces réservés pour les véritables noms, tels que *lit View*.

> [!Note]  
> à partir de Windows 8, le nom utilisé pour l’inscription pour les paramètres par défaut de l’accès aux programmes et de l' [ordinateur (SPAD)](cpl-setprogramaccess.md) et pour les [programmes par défaut](default-programs.md) doit correspondre pour que les modifications de SPAD déclenchent les inscriptions des programmes par défaut.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

La valeur **LocalizedString** est une \_ chaîne sz reg et se compose d’un signe « at » (@), du chemin d’accès complet à un fichier .dll ou .exe, d’une virgule, d’un signe moins et d’un entier décimal. L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans le fichier .dll ou .exe, dont la valeur doit être affichée à l’utilisateur en tant que nom de ce client. Notez que le chemin d’accès du fichier ne requiert pas de guillemets, même s’il contient des espaces.

L’inscription de la chaîne de nom complet de cette manière permet d’utiliser la même inscription pour plusieurs langues. Chaque installation de langue fournit un fichier de ressources différent avec le nom complet stocké au même ID de ressource.

L’exemple suivant illustre l’inscription d’un programme de messagerie instantanée éclairé. Étant donné qu’il s’agit d’un programme de messagerie instantanée, la sous-clé *CanonicalName* (dans ce cas, *lit la vue*) est stockée sous la sous-clé **im** .

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Notez l’utilisation de l’entrée (par défaut) comme déclaration secondaire du nom complet du client. Si le **LocalizedString** n’est pas présent, la valeur (par défaut) est utilisée à la place. Cela fonctionne avec tous les types de clients (navigateurs Internet, navigateurs de messagerie, messagerie instantanée et lecteurs multimédias). Pour assurer la compatibilité descendante avec la [disposition du Registre du client Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), les programmes de messagerie doivent définir la valeur (par défaut) de la sous-clé *CanonicalName* sur le nom d’affichage du client dans la langue actuellement installée.

### <a name="registering-a-programs-icon"></a>Inscription de l’icône d’un programme

> [!Note]  
> cette section ne s’applique pas à Windows 2000.

 

par défaut, la section supérieure du menu **démarrer** de Windows XP et Windows Vista contient des icônes **Internet** et de **messagerie** . ces icônes ne sont pas présentes dans Windows 7 et versions ultérieures. Pour les clients de messagerie et de navigateur, lorsqu’un programme est attribué par défaut à son type de client, l’icône inscrite de ce programme s’affiche pour ces entrées de menu **Démarrer** .

L’inscription de l’icône d’un programme est obligatoire pour les clients de messagerie et de navigateur. l’inscription d’une icône pour la lecture du média, la messagerie instantanée ou la machine virtuelle pour les types de clients Java est facultative, et les icônes inscrites pour ces types de clients ne sont pas utilisées actuellement par Windows et ne sont pas affichées dans la section supérieure des menus **démarrer** Windows XP ou Windows Vista.

Pour inscrire une icône pour un programme client, ajoutez une sous-clé **DefaultIcon** avec une valeur par défaut, comme indiqué ici.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

La valeur **filePath** est le chemin d’accès complet au fichier qui contient l’icône. Ce chemin d’accès ne requiert pas de guillemets, même s’il contient des espaces.

La valeur **IndexIcône** est interprétée comme suit :

-   Si **IndexIcône** est un nombre positif, le nombre est utilisé comme index du tableau de *base zéro* des icônes stockées dans le fichier. Par exemple, si **IndexIcône** est 1, la deuxième icône est chargée à partir du fichier.
-   Si **IndexIcône** est un nombre négatif, la valeur absolue de **IndexIcône** est utilisée comme identificateur de ressource (plutôt que l’index) pour l’icône. Par exemple, si **IndexIcône** est-3, l’icône dont l’identificateur de ressource est 3 est chargée à partir du fichier.

L’exemple suivant illustre l’inscription d’un navigateur d’affichage lit hypothétique. La deuxième icône stockée dans le fichier Litview.exe est utilisée comme valeur par défaut.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Inscription d’un verbe ouvert

> [!Note]  
> cette section ne s’applique pas à Windows 2000. L’étape suivante est nécessaire uniquement pour les clients de messagerie et de navigateur.

 

Supposons qu’un utilisateur a sélectionné votre programme comme programme Internet ou de messagerie par défaut. cet utilisateur clique sur l’icône **Internet** ou **courrier électronique** dans le menu **démarrer** de Windows XP ou Windows Vista pour ouvrir le programme. À ce stade, la ligne de commande enregistrée comme indiqué ici est exécutée.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

La ligne de commande doit spécifier un chemin d’accès absolu complet au fichier, suivi d’options de ligne de commande facultatives. Si le type d’entrée est REG \_ expand \_ SZ, les variables d’environnement peuvent être utilisées dans le chemin d’accès. Utilisez des guillemets pour vous assurer que les espaces dans la ligne de commande ne sont pas interprétés de manière incorrecte. La ligne de commande doit exécuter le programme avec les valeurs par défaut appropriées. Les navigateurs sont généralement par défaut sur la page d’hébergement de l’utilisateur. Les programmes de messagerie ouvrent généralement la **boîte de réception** de l’utilisateur.

L’exemple suivant illustre l’inscription d’un `open` verbe pour un Explorateur d’affichages hypothétique. Elle ne spécifie aucune option de ligne de commande.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Notez que, dans cette valeur, des guillemets sont placés autour du chemin d’accès, car il contient des espaces incorporés. Si vous omettez ces guillemets, la ligne de commande risque d’être interprétée à tort.

### <a name="registering-installation-information"></a>Inscription des informations d’installation

> [!Note]  
> cette section ne s’applique pas à Windows Server 2003.

 

-   [Commande de réinstallation](#the-reinstall-command)
-   [Commande masquer les icônes](#the-hide-icons-command)
-   [Commande Afficher les icônes](#the-show-icons-command)
-   [Configuration du programme de groupe](#group-program-configuration)
-   [Exemple d’inscription de navigateur](#browser-registration-example)

La fonctionnalité par laquelle l’utilisateur sélectionne les programmes par défaut par ordinateur est nommée et accessible comme indiqué dans le tableau suivant. (Windows Vista a introduit une nouvelle fonctionnalité, **défini vos programmes par défaut**, par lequel un utilisateur peut définir des valeurs par défaut par utilisateur.)




| Système d’exploitation | Titre | Emplacement d’accès | 
|------------------|-------|-----------------|
| Windows 7 | Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur | <ul><li>Option <strong>programmes par défaut</strong> du menu <strong>Démarrer</strong></li><li><strong>Programmes par défaut</strong> Élément du panneau de configuration</li></ul> | 
| Windows Vista | Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur | <ul><li>Option <strong>programmes par défaut</strong> du menu <strong>Démarrer</strong></li><li><strong>Programmes par défaut</strong> Élément du panneau de configuration</li></ul> | 
| Windows XP SP2 | Définir l’accès aux programmes et les valeurs par défaut | <ul><li>Menu <strong>Démarrer</strong></li><li><strong>Ajout/suppression de programmes</strong> Élément du panneau de configuration</li></ul> | 
| Windows XP SP1 | Configurer des programmes | <ul><li><strong>Ajout/suppression de programmes</strong> Élément du panneau de configuration</li></ul> | 




 

par souci de simplicité, cette rubrique utilise le titre Windows 7 de la fonctionnalité. Toutes les versions de la fonctionnalité sont communément appelées SPAD.

> [!Note]  
> si vous exécutez Windows 2000 ou Windows xp, vous devez disposer d’au moins Windows 2000 SP3 ou Windows xp SP1 pour voir la page **définir l’accès aux programmes et aux valeurs par défaut** . dans Windows Vista et versions ultérieures, l’accès à la page **définir les paramètres par défaut de l’accès aux programmes et des ordinateurs** requiert des privilèges d’administrateur. Pour cette raison, les développeurs sont encouragés à s’inscrire pour l’élément définir votre panneau de configuration [programmes par défaut](default-programs.md) afin que n’importe quel utilisateur puisse gérer les valeurs par défaut de l’application.

 

L’arborescence de Registre suivante affiche la variété des informations qui doivent être inscrites dans la clé **InstallInfo** du programme pour que le programme s’affiche sur la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur en tant qu’option pour son type de client. Chacune de ces valeurs est décrite en détail dans les sections suivantes.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

La ligne de commande doit spécifier un chemin d’accès absolu complet au fichier, suivi d’options de ligne de commande facultatives. Utilisez des guillemets pour vous assurer que les espaces dans la ligne de commande ne sont pas interprétés de manière incorrecte.

### <a name="the-reinstall-command"></a>Commande de réinstallation

La ligne de commande de réinstallation déclarée dans la valeur ReinstallCommand est exécutée lorsque l’utilisateur utilise la page **définir les paramètres par défaut de l’accès aux programmes et des ordinateurs** pour sélectionner votre programme comme type de client par défaut. dans Windows Vista et versions ultérieures, l’accès à cette page nécessite un niveau de privilège d’administrateur. dans Windows 8, si vous avez inscrit votre application en utilisant le même nom pour **définir l’accès aux programmes et les paramètres par défaut** de l’ordinateur et **par** défaut, les valeurs par défaut spécifiées dans **programmes par défaut** pour cette application seront appliquées à l’utilisateur actuel, ainsi que l’exécution de la commande réinstaller.

Le programme lancé par la ligne de commande de réinstallation doit associer l’application à l’ensemble complet de types de [fichiers](fa-intro.md) et de [protocoles](/previous-versions//aa767743(v=vs.85)) que l’application peut gérer. Toutes les applications doivent mettre en place une fonctionnalité de gestionnaire dans la commande de réinstallation. Les applications peuvent utiliser la commande réinstaller pour inscrire la fonctionnalité et éventuellement établir l’État par défaut. Quand une application choisit d’implémenter les fonctionnalités et l’état du gestionnaire par défaut dans la commande de réinstallation, elle doit également rétablir les liens ou les raccourcis visibles souhaités. Les points d’entrée visibles pour la plupart des applications sont répertoriés dans [la commande masquer les icônes](#the-hide-icons-command).

> [!Note]  
> Il est vivement recommandé que les applications implémentent la fonctionnalité de gestion dans la commande de réinstallation.

 

Une fois le processus de réinstallation terminé, le programme lancé par la ligne de commande de réinstallation doit s’arrêter. Il ne doit pas lancer le programme correspondant. il doit simplement enregistrer les valeurs par défaut. Par exemple, la commande de réinstallation d’un navigateur ne doit pas ouvrir la page d’hébergement de l’utilisateur.

> [!Note]  
> pour les clients de messagerie et de navigateur dans Windows XP et Windows Vista, les applications qui choisissent d’établir la capacité de gestion et l’état par défaut dans la commande de réinstallation doivent s’inscrire à l’icône correspondante en haut du menu Démarrer. Pour plus d’informations, consultez [enregistrement du menu Démarrer](#start-menu-registration) .

 

### <a name="the-hide-icons-command"></a>Commande masquer les icônes

La ligne de commande déclarée dans la valeur HideIconsCommand est exécutée lorsque l’utilisateur désactive l’option **activer l’accès à ce programme** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur. Cette ligne de commande doit masquer tous les points d’accès de votre programme qui sont visibles dans l’interface utilisateur. Les instructions spécifiques sont de supprimer des raccourcis et des icônes à partir des emplacements suivants :

-   Icônes de bureau
-   liens menu Démarrer, y compris le groupe de **démarrage**
-   Liens vers la barre de lancement rapide
-   Zone Notifications
-   Menus contextuels
-   Bande de tâches du dossier

Cette ligne de commande doit également empêcher les appels automatiques du programme, tels que ceux spécifiés dans la clé de Registre **Run** . Les fournisseurs sont encouragés à implémenter ces instructions dans le rappel d’accès de masquage de l’application.

Vous n’avez pas besoin d’abandonner l’inscription (fonctionnalité d’application) des types de fichiers lorsque les icônes sont masquées. Vous n’avez pas non plus besoin de renoncer à l’État par défaut de l’application pour les types de fichiers et de protocoles. Cela peut entraîner une mauvaise expérience utilisateur lorsque ces types sont rencontrés dans l’interface utilisateur.

Après avoir masqué correctement les icônes, vous devez mettre à jour la valeur de Registre IconsVisible sur 0 comme indiqué ci-dessous :

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

L’entrée IconsVisible est de type **reg \_ DWORD**.

### <a name="an-alternate-hide-icons-method-in-spad"></a>Une autre méthode masquer les icônes dans SPAD

Pour certaines applications héritées, une implémentation complète de l’accès masqué peut ne pas être pratique. Une autre méthode qui atteint le même effet consiste à désinstaller l’application. La section ci-dessous montre un exemple de comportement et un exemple de code pour implémenter cette alternative. En général, les éditeurs de logiciels indépendants doivent éviter cette alternative, car ils :

-   Désinstallez complètement l’application du système.
-   Supprimer les valeurs par défaut précédemment sélectionnées.
-   Ne laissez aucune option d’interface utilisateur pour réinstaller l’application.
-   Rendez la fonctionnalité activer l’accès plus disponible, car une désinstallation supprime complètement l’application de SPAD.

L’expérience utilisateur recommandée est la suivante :

-   Lorsque l’utilisateur décoche la case **activer l’accès à ce programme** dans SPAD, l’interface utilisateur suivante est présentée.

    ![boîte de dialogue à propos du masquage de l’accès au programme](images/hideaccessvista.png)

-   Quand l’utilisateur clique sur **OK**, l’élément **programmes et fonctionnalités** du panneau de configuration démarre pour permettre à l’utilisateur de désinstaller l’application.
-   Windows Les utilisateurs XP doivent être affichés dans cette boîte de dialogue.

    ![boîte de dialogue Windows XP équivalente](images/hideaccessxp.png)

-   lorsque l’utilisateur Windows XP sélectionne **OK**, l’élément **ajouter ou supprimer des programmes** du panneau de configuration démarre pour permettre à l’utilisateur de désinstaller l’application.

Le code suivant fournit une implémentation réutilisable pour la fonctionnalité masquer l’accès, comme indiqué ci-dessus. il peut être utilisé sur Windows XP, Windows Vista et Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>Commande Afficher les icônes

La ligne de commande déclarée dans l’entrée ShowIconsCommand est exécutée lorsque l’utilisateur coche la case **activer l’accès à ce programme** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur. Cette ligne de commande peut restaurer les points d’accès de votre programme, y compris ceux qui se trouvent dans le menu **Démarrer** , sur le bureau et dans le groupe **démarrage** , ainsi que les appels automatiques normaux, tels que ceux spécifiés dans la clé de Registre **Run** . Les points d’accès visibles intéressants pour la plupart des applications sont répertoriés dans [la commande masquer les icônes](#the-hide-icons-command). L’application ne doit pas modifier les valeurs par défaut par utilisateur ; Cette modification doit être effectuée par l’utilisateur par le biais de **programmes par défaut**.

Une fois vos icônes correctement affichées, vous devez mettre à jour la valeur de Registre IconsVisible sur 1, comme indiqué ci-dessous :

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Notez que si vous avez utilisé l’entrée HideIconsCommand pour inviter une désinstallation de l’application, l’entrée ShowIconsCommand n’est pas utilisée. Elle doit être supprimée du Registre avec le reste des informations de l’application pendant le processus de désinstallation.

### <a name="group-program-configuration"></a>Configuration du programme de groupe

> [!Note]  
> cette section ne s’applique pas à Windows 2000.

 

Dans le cadre de la préparation du système, un fabricant d’ordinateurs OEM peut établir une configuration qui masque les points d’accès pour les programmes du navigateur, de la messagerie, de la lecture multimédia, de la messagerie instantanée ou de la machine virtuelle Microsoft pour les programmes clients Java et spécifie leurs propres programmes par défaut. Les fabricants OEM peuvent permettre aux utilisateurs de réinitialiser leurs ordinateurs à tout moment dans cette configuration par défaut en définissant les valeurs de Registre suivantes.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Si ces clés sont définies, les utilisateurs peuvent restaurer la configuration OEM en sélectionnant l’option fabricant de l' **ordinateur** dans la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur. Si ces clés ne sont pas définies, l’option fabricant de l' **ordinateur** n’est pas affichée.

L’entrée **OEMShowIcons** , si elle est présente, définit l’état de l’icône afficher pour le client spécifié qui est appliqué si l’utilisateur sélectionne fabricant de l' **ordinateur**. La valeur 1 entraîne l’affichage des icônes, tandis que la valeur 0 provoque l’absence d’affichage des icônes. Si **OEMShowIcons** est absent, le fait de sélectionner le fabricant de l' **ordinateur** n’a aucun effet sur l’icône Afficher le paramètre. **OEMShowIcons** est de type **reg \_ DWORD**.

L’entrée **OEMDefault** , si elle est présente et définie sur 1, définit la préférence OEM pour le client par défaut du type indiqué. Un seul client d’un type particulier peut être marqué comme valeur par défaut OEM. Si plus d’une inscription du client contient l’entrée **OEMDefault** , tous sont ignorés et le client actuel continue à être utilisé comme client par défaut. Si l’entrée **OEMDefault** est absente ou présente et définie sur 0, ce client particulier n’est pas utilisé comme client par défaut si l’utilisateur sélectionne **Computer Manufacturer**. **OEMDefault** est de type **reg \_ DWORD**.

Outre l’option de réinitialisation de leurs ordinateurs à la configuration par défaut établie par l’OEM, les utilisateurs disposent de trois autres options de configuration :

-   définissez l’ordinateur sur une configuration Microsoft Windows. Dans ce cas, la page **définir les paramètres par défaut de l’accès aux programmes et** de l’ordinateur permet d’accéder à tous les logiciels Microsoft et non-Microsoft sur l’ordinateur inscrit dans les catégories de produits appropriées. les programmes Microsoft Windows sont sélectionnés comme option par défaut pour chaque catégorie.
-   Définissez leur ordinateur sur une configuration non-Microsoft. cette configuration masque les points d’accès (tels que le menu **démarrer** ) à Windows Internet Explorer, Lecteur Windows Media, Windows Messenger et Microsoft Outlook Express. Il permet d’accéder aux logiciels non-Microsoft sur l’ordinateur dans ces catégories. En outre, si un programme non-Microsoft est disponible dans une catégorie, il est défini comme valeur par défaut pour cette catégorie. Si plusieurs programmes non-Microsoft sont disponibles dans une catégorie, l’utilisateur est invité à choisir le programme non-Microsoft qui doit être utilisé par défaut.
-   Établissez une configuration personnalisée. Les utilisateurs effectuent leurs propres sélections pour l’activation ou la suppression de l’accès, en mélangeant les programmes Microsoft et non-Microsoft comme ils le voient. Les utilisateurs établissent des options par défaut en fonction de la catégorie.

Les utilisateurs sont libres de modifier ces options à tout moment.

### <a name="browser-registration-example"></a>Exemple d’inscription de navigateur

L’exemple suivant montre l’inscription **InstallInfo** complète pour un navigateur de vue éclairé de façon fictive. Dans ce cas, les commutateurs de ligne de commande permettent au fichier Litview.exe d’effectuer toutes les actions nécessaires pour chaque valeur.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Notez que les guillemets sont placés autour des tracés, car ils contiennent des espaces incorporés.

## <a name="registration-elements-for-specific-client-types"></a>Éléments d’inscription pour des types de client spécifiques

Vous trouverez également les informations suivantes dans les ressources figurant dans la section Rubriques connexes à la fin de cette rubrique.

-   [Enregistrement du menu Démarrer](#start-menu-registration)
-   [Inscription du client de messagerie](#mail-client-registration)

### <a name="start-menu-registration"></a>Enregistrement du menu Démarrer

sous Windows XP, les applications sont généralement inscrites par défaut sur un ordinateur (**hkey \_ LOCAL \_ machine**) plutôt que sur l’étendue utilisateur (**hkey \_ CURRENT \_ user**). avec l’introduction Windows Vista du contrôle de compte d’utilisateur, les applications qui réclament l' **Internet** et les emplacements de **messagerie** dans le menu **démarrer** doivent implémenter la commande de réinstallation dans le contexte d’exécution approprié.

> [!Note]  
> le lien menu Démarrer **E-mail** a été supprimé à partir de Windows 7. Toutefois, l’inscription décrite dans cette section doit toujours être effectuée, car elle affecte le client MAPI par défaut.

 

un utilisateur limité sur Windows XP, Windows Vista ou Windows 7 ne peut pas accéder à SPAD. Pour cette raison, les développeurs sont encouragés à s’inscrire à l’élément **définir vos programmes par défaut** du panneau de configuration afin que n’importe quel utilisateur puisse gérer les valeurs par défaut des applications par utilisateur.

Les sélections effectuées dans SPAD doivent uniquement affecter les paramètres par ordinateur.

Définissez la valeur de Registre comme suit.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **les informations suivantes s’appliquent uniquement à Windows XP.**
> 
> Si l’inscription de la valeur par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus est réussie, l’application doit supprimer la valeur assignée à l’entrée par défaut sous la sous-clé suivante :
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Si l’inscription de la valeur par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus échoue, généralement parce que l’utilisateur n’a pas d’autorisation d’écriture sur la sous-clé, l’application doit définir la valeur suivante :
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> Cela enregistre le nom canonique uniquement pour l’utilisateur actuel, et non pour tous les utilisateurs.

 

Après la mise à jour des clés de Registre, le programme doit diffuser le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec **wParam** = 0 et **lParam** pointant vers la chaîne terminée par le caractère null « \\ clients logiciels \\ **ClientTypeName**» pour notifier le système d’exploitation que le client par défaut a changé.

### <a name="mail-client-registration"></a>Inscription du client de messagerie

Pour un client de messagerie, le programme doit avoir des paramètres enregistrés sous la clé de clé mailto de la **\_ \_ racine de classes HKEY** \\  pour pouvoir traiter les URL qui utilisent le `mailto` protocole. Définissez les valeurs et les clés qui reflètent ces paramètres sous la clé suivante.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Cette hiérarchie de Registre remplace la `mailto` hiérarchie de Registre existante trouvée dans **HKEY \_ classes \_ root** \\ **mailto**. La hiérarchie reste la même, seul l’emplacement a changé. Le format de cette hiérarchie est documenté sur MSDN sous [vues d’ensemble et didacticiels de protocoles enfichables asynchrones](/previous-versions//aa767913(v=vs.85)). En règle générale, le `mailto` protocole est inscrit à un programme plutôt qu’à un protocole asynchrone, auquel cas la documentation sur l' [enregistrement d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) s’applique.

L’exemple suivant illustre la `mailto` section de l’inscription d’un `mailto` Gestionnaire inscrit auprès d’un programme.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

La valeur de Registre indicateurs est documentée dans les [types de fichiers](fa-file-types.md) de la section intitulée « définition des attributs de type de fichier ».

## <a name="complete-sample-registrations"></a>Compléter les exemples d’inscriptions

Les exemples suivants sont fournis pour montrer les exigences d’inscription complètes pour les différents types de clients.

-   [Exemple de navigateur](#a-sample-browser)
-   [Exemple de navigateur de messagerie](#a-sample-mail-browser)
-   [Exemple de lecteur multimédia](#a-sample-media-player)
-   [Exemple de programme Instant Messenger](#a-sample-instant-messenger-program)
-   [Exemple de machine virtuelle Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Exemple de navigateur

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Exemple de navigateur de messagerie

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Exemple de lecteur multimédia

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Exemple de programme Instant Messenger

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Exemple de machine virtuelle Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*Les exemples de sociétés, d’organisations, de produits, de noms de domaine, d’adresses de messagerie, de logos, de personnes, de lieux et d’événements mentionnés dans les exemples sont fictifs. Toute ressemblance avec des sociétés, des organisations, des produits, des noms de domaine, des adresses électroniques, des logos, des personnes, des lieux ou des événements réels est purement fortuite et involontaire.*

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Programmes par défaut](default-programs.md)
</dt> <dt>

[comment inscrire un navigateur Internet ou un Client de messagerie à l’aide du Menu démarrer Windows](start-menu-reg.md)
</dt> <dt>

[Disposition du Registre du client Internet Explorer (voir la section « Définitions des clés de Registre du client »)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Vues d’ensemble et didacticiels enfichables de protocoles enfichables asynchrones](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Inscription d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
