---
description: Le menu Démarrer de Windows XP et Windows Vista contient des emplacements réservés pour les clients Internet (navigateur) et de messagerie électronique (messagerie) par défaut, communément appelés applications Internet du menu Démarrer.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211298"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows

> [!Note]  
> Cette rubrique s’applique à Windows XP, Windows Vista et Windows 7.

 

Le menu Démarrer de Windows XP et Windows Vista contient des emplacements réservés pour les clients **Internet** (navigateur) et de **messagerie électronique** (messagerie) par défaut, communément appelés *applications Internet du menu Démarrer*. Les applications qui s’inscrivent en tant qu’applications Internet du menu Démarrer le font sur l’ensemble du système (par ordinateur). Dans Windows Vista, l’utilisateur peut utiliser la fonctionnalité **programmes par défaut** pour définir une valeur par défaut pour chaque utilisateur.

Lorsque les applications s’inscrivent en tant qu’applications Internet du menu Démarrer, Windows XP et Windows Vista créent des icônes **Internet** et de **messagerie électronique** dans le menu Démarrer. En cliquant sur ces icônes, le menu Démarrer vérifie la sous-arborescence du Registre par utilisateur (**HKEY \_ Current \_ User**). Si aucun paramètre par défaut par utilisateur n’est trouvé, le menu Démarrer recherche la sous-clé par défaut par ordinateur dans la sous-arborescence de l' **\_ \_ ordinateur local HKEY** .

> [!Note]  
> L’installation par défaut de Windows n’inscrit pas un programme Internet ou de messagerie par défaut par utilisateur, mais uniquement une valeur par défaut à l’ensemble du système. Cela offre un chemin de mise à niveau fluide à partir des versions précédentes du système d’exploitation, dans lequel seule la sous-arborescence de la \_ machine locale HKEY \_ est prise en charge pour les inscriptions du client.

 

Cette rubrique présente les éléments suivants :

-   [Inscription pour le lien Internet du menu Démarrer](#registering-for-the-start-menu-internet-link)
    -   [Comment s’inscrire en tant que client Internet par défaut](#how-to-register-as-the-default-internet-client)
-   [Inscription pour le lien de messagerie du menu Démarrer](#registering-for-the-start-menu-email-link)
    -   [Comment le menu Démarrer affiche le client de messagerie par défaut](#how-the-start-menu-displays-the-default-email-client)
    -   [Comment s’inscrire en tant que client de messagerie par défaut](#how-to-register-as-the-default-email-client)
-   [Personnalisation du menu contextuel](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Inscription pour le lien Internet du menu Démarrer

> [!Note]  
> Cette inscription est déconseillée à partir de Windows 7, qui ne fournit plus de lien Internet dans le menu Démarrer. Les inscriptions existantes sont ignorées dans Windows 7 et les versions ultérieures. L’inscription de l’application Internet par défaut dans le menu Démarrer n’est pas la même que celle du navigateur Web par défaut. Le navigateur Web par défaut est utilisé pour lancer des URL arbitraires depuis n’importe où dans le système. L’application Internet du menu Démarrer contrôle simplement le programme qui est démarré lorsque l’utilisateur clique sur l’icône Internet dans le menu Démarrer.

 

Toute application de navigateur Web peut s’inscrire pour apparaître en tant que client Internet dans le menu Démarrer. Cette visibilité, couplée à une inscription correcte pour les types de [fichier](fa-intro.md) et de [protocole](/previous-versions//aa767743(v=vs.85)) d’une application, donne un État du navigateur par défaut de l’application.

Les inscriptions effectuées dans la sous-arborescence de la sous-arborescence de l' **\_ \_ utilisateur actuel** ont une priorité plus élevée pour l’utilisateur de la console que les inscriptions correspondantes effectuées sur l' **\_ \_ ordinateur local HKEY**. Pour les nouveaux utilisateurs sur le système, les paramètres stockés dans **HKEY \_ local \_ machine** sont utilisés. À compter de Windows XP, le menu démarrer les paramètres Internet sont conservés dans les entrées par défaut de deux emplacements du Registre :

-   **HKEY \_ Clients du logiciel \_ utilisateur actuel** \\  \\  \\ **StartMenuInternet**
-   **HKEY \_ \_** Clients de logiciels de l’ordinateur local \\  \\  \\ **StartMenuInternet**

La sous-clé **HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\ **StartMenuInternet** décrit le navigateur Internet qui est démarré lorsque l’utilisateur clique sur l’icône **Internet** dans le menu Démarrer. Si cette sous-clé est vide ou manquante, l’icône **Internet** dans le menu Démarrer est définie sur la valeur système par défaut stockée dans le deuxième emplacement de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** , qui décrit toutes les applications de navigateur Internet installées sur le système.

Quand un nouvel utilisateur se connecte au système, le menu Démarrer utilise la valeur par défaut dans la sous-clé de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** pour afficher le client Internet par défaut et démarrer l’application inscrite lorsque l’utilisateur clique sur cette icône.

### <a name="how-to-register-as-the-default-internet-client"></a>Comment s’inscrire en tant que client Internet par défaut

Sous la sous-clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** , il peut y avoir zéro, une ou plusieurs sous-clés, une pour chaque application de navigateur Internet inscrite. Par exemple, un système hypothétique peut avoir cette organisation :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Nous présenterons les entrées de Registre avec un navigateur hypothétique appelé « lit View » à partir d’une société fictive appelée Litware Inc. Supposons que le nom de l’exécutable pour lit View est Litview.exe. L’inscription de la vue lit se produit comme indiqué ici :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Les données LocalizedString sont de type REG \_ SZ, ou reg \_ expand \_ SZ si les variables de chemin d’accès telles que `%programfiles%` sont utilisées. LocalizedString fournit le chemin d’un fichier exécutable (. exe) ou d’un fichier de bibliothèque (. dll). Notez que la chaîne de chemin d’accès commence par un signe « at » (@) et qu’aucun guillemet n’est requis autour du chemin d’accès, quels que soient les espaces qu’il contient. L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans la DLL spécifiée, dont la valeur doit être affichée à l’utilisateur. Cela permet d’utiliser la même inscription pour plusieurs langues. Chaque langue fournit une ResourceDLL.dll différente. Cela permet au système d’afficher la chaîne correcte en fonction de la langue actuellement sélectionnée.

La \_ valeur de l’option reg SZ ou reg \_ expand développée suivante \_ indique au menu Démarrer de l’icône par défaut de s’afficher lorsque l’utilisateur sélectionne l’affichage allumé comme menu Démarrer navigateur Internet.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

La sous-clé de Registre suivante spécifie une ligne de commande à exécuter quand l’utilisateur clique sur la commande de menu Internet dans le menu Démarrer, en supposant que lit View est le navigateur Internet sélectionné pour le menu Démarrer. Par exemple, la commande peut ouvrir le navigateur avec la page d’hébergement de l’utilisateur, ou la commande peut lancer une interface utilisateur d’introduction que l’éditeur de logiciels indépendant (ISV) estime être approprié. Les données sont de type REG \_ SZ ou reg \_ expand \_ SZ, mais notez qu’étant donné qu’il y a un espace dans le chemin d’accès à la ligne de commande, le chemin d’accès de l’exécutable est placé entre guillemets.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

Lorsque l’utilisateur spécifie par le biais de l’option [définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) qui lit l’affichage doit être utilisé comme navigateur Web par défaut au niveau de l’ordinateur, l’application doit définir l’entrée de Registre \_ SZ suivante. Notez que le paramètre SPAD s’exécutant avec des privilèges d’administrateur, l’accès à cette sous-clé est autorisé.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> Dans Windows Vista, le navigateur Web par défaut au niveau de l’utilisateur doit être défini à l’aide de l’outil **programmes par défaut** , et non de [SPAD](cpl-setprogramaccess.md).
> 
> **Les informations suivantes s’appliquent uniquement à Windows XP.**
> 
> Si l’inscription du navigateur Web par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine comme indiqué ci-dessus réussit, l’application doit supprimer l’entrée par défaut sous la sous-clé suivante :
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Si l’inscription du navigateur Web par défaut au niveau de l’ordinateur sous HKEY \_ local \_ machine échoue, l’application doit définir les données de reg \_ SZ comme indiqué dans cet exemple pour l’application de vue allumée :
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Après la mise à jour des sous-clés appropriées, l’application diffuse le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec son paramètre *wParam* défini sur 0 et son paramètre *lParam* pointant vers la chaîne terminée par le caractère null `"Software\Clients\StartMenuInternet"` . Cela indique au système d’exploitation que le client par défaut a changé.

La définition de ces sous-clés pour le menu démarrer par défaut navigateur Internet est nécessaire pour préserver la compatibilité descendante avec les anciens navigateurs Web qui ne prennent pas en charge les inscriptions par utilisateur.

## <a name="registering-for-the-start-menu-email-link"></a>Inscription pour le lien de messagerie du menu Démarrer

> [!Note]  
> Le lien de messagerie du menu Démarrer a été supprimé à partir de Windows 7. Toutefois, cette inscription décrite dans cette section doit toujours être effectuée pour son effet lors de l’attribution du client MAPI par défaut.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Comment le menu Démarrer affiche le client de messagerie par défaut

Toutes les applications de messagerie peuvent s’inscrire pour apparaître en tant que client de messagerie dans le menu Démarrer. Cette visibilité, couplée à une inscription correcte pour les types de [fichier](fa-intro.md) et de [protocole](/previous-versions//aa767743(v=vs.85)) d’une application, donne l’état de messagerie par défaut de l’application.

Les inscriptions effectuées dans la sous-arborescence de la sous-arborescence de l' **\_ \_ utilisateur actuel** ont une priorité plus élevée pour l’utilisateur de la console que les inscriptions correspondantes effectuées sur l' **\_ \_ ordinateur local HKEY**. Pour les nouveaux utilisateurs sur le système, les paramètres stockés dans **HKEY \_ local \_ machine** sont utilisés. À compter de Windows XP, les paramètres de messagerie du menu Démarrer sont conservés dans les entrées par défaut de deux emplacements du Registre :

-   **HKEY \_ \_** Messagerie des \\  \\ **clients** \\  logiciels des utilisateurs actuels
-   **HKEY \_ \_** Messagerie des \\  \\ **clients** \\  logiciels de l’ordinateur local

La sous-clé **HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\ **mail** décrit le client de messagerie qui est démarré lorsque l’utilisateur clique sur l’icône de **courrier électronique** dans le menu Démarrer.

La sous-clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** décrit les applications de messagerie qui sont installées sur le système, ainsi que l’application de messagerie par défaut.

Si la **messagerie HKEY \_ Current \_ User** \\ **Software** \\ **clients** \\  est vide ou manquante, la valeur par défaut définie dans **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** est utilisée pour sélectionner l’application de messagerie qui apparaît dans le menu Démarrer.

Quand un nouvel utilisateur se connecte au système, le menu Démarrer utilise la valeur par défaut dans la sous-clé de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** pour afficher le client de messagerie par défaut et démarre l’application inscrite lorsque l’utilisateur clique sur cette icône.

### <a name="how-to-register-as-the-default-email-client"></a>Comment s’inscrire en tant que client de messagerie par défaut

**HKEY \_ La \_** \\  \\  \\ **messagerie** des clients de logiciels de l’ordinateur local peut contenir zéro, une ou plusieurs sous-clés, une pour chaque application de messagerie inscrite. Par exemple, un système hypothétique peut définir les sous-clés suivantes :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

Nous présenterons les entrées de Registre avec un client de messagerie hypothétique appelé « lit mail » de la société fictive nommée Litware Inc. Litware Inc. Décide d’inscrire ce client de messagerie sous le nom interne « LitMail ». Comme avec un navigateur, le nom interne est une chaîne unique utilisée comme nom de sous-clé, mais elle n’est jamais affichée à l’utilisateur.

Pour installer le client de messagerie lit mail comme par défaut, il utilise la sous-clé suivante et ses entrées :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

Les données LocalizedString sont de type REG \_ SZ, ou reg \_ expand \_ SZ si les variables de chemin d’accès telles que `%programfiles%` sont utilisées. LocalizedString fournit le chemin d’un fichier exécutable (. exe) ou d’un fichier de bibliothèque (. dll). Notez que la chaîne de chemin d’accès commence par un signe « at » (@) et qu’aucun guillemet n’est requis autour du chemin d’accès, quels que soient les espaces qu’il contient. L’entier décimal est l’ID d’une ressource de type chaîne, contenue dans la DLL spécifiée, dont la valeur doit être affichée à l’utilisateur. Cela permet d’utiliser la même inscription pour plusieurs langues. Chaque langue fournit une ResourceDLL.dll différente. Cela permet au système d’afficher la chaîne correcte en fonction de la langue actuellement sélectionnée.

Après la mise à jour des sous-clés appropriées, l’application diffuse le message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) avec son paramètre *wParam* défini sur 0 et son paramètre *lParam* pointant vers la chaîne terminée par le caractère null `"Software\Clients\Mail"` . Cela indique au système d’exploitation que le client par défaut a changé.

Pour assurer la compatibilité descendante avec les applications qui ne prennent pas en charge les chaînes localisées, le nom de l’application dans la langue installée doit également être défini comme valeur par défaut de la sous-clé.

La valeur de la commande **reg \_ SZ** ou **reg \_ expand développée \_** suivante indique au menu Démarrer de l’icône par défaut de s’afficher lorsque l’utilisateur sélectionne lit mail comme programme de messagerie du menu Démarrer :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

L’entrée suivante spécifie une ligne de commande à exécuter lorsque l’utilisateur clique sur l’élément de menu de **messagerie** dans le menu Démarrer, en supposant que lit mail est le programme de messagerie du menu Démarrer sélectionné. Cette ligne de commande s’exécute également si l’utilisateur sélectionne **lire le courrier électronique** dans le menu **Outils** de Windows Internet Explorer. Les données sont de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, mais notez qu’étant donné qu’il y a un espace dans le chemin d’accès à la ligne de commande, le chemin d’accès de l’exécutable est placé entre guillemets.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

Si (et seulement si) *l’utilisateur* spécifie lit mail comme l’application de messagerie du menu démarrer par défaut, l’application de messagerie lit peut écrire son nom interne à la valeur de **reg \_ SZ** suivante :

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Si (et seulement si) *l’utilisateur* spécifie lit mail comme étant l’application de messagerie par défaut au niveau du système, l’application lit mail peut écrire son nom interne sur la valeur **reg \_ SZ** spécifiée ci-dessous. Notez que l’accès à cette sous-clé peut être restreint. Les applications ne doivent pas supposer que tous les utilisateurs sont autorisés à modifier l’application de messagerie par défaut au niveau du système.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

L’inscription en tant qu’application de messagerie du menu démarrer par défaut n’est pas équivalente à l’inscription en tant que client de messagerie par défaut système ou le gestionnaire *mailto* inscrit.

-   Le client de messagerie par défaut du système est démarré lorsque l’utilisateur clique sur **lire le courrier électronique** dans le menu **Outils** d’Internet Explorer.
-   Le gestionnaire *mailto* inscrit est démarré lorsque l’utilisateur clique sur une URL au format `mailto:someone@example.com` .
-   L’application de messagerie du menu Démarrer démarre lorsque l’utilisateur clique sur l’icône de **courrier électronique** dans le menu Démarrer.

Si aucune application de messagerie du menu démarrer par défaut n’est spécifiée, l’icône de courrier électronique dans le menu Démarrer lance le client de messagerie par défaut du système.

Cette rubrique ne couvre pas l’inscription de l’application en tant que gestionnaire de protocole *mailto* par défaut. Les applications qui veulent s’inscrire de cette manière doivent continuer à suivre les spécifications existantes sur ce sujet.

## <a name="customizing-the-context-menu"></a>Personnalisation du menu contextuel

Une application peut personnaliser les pages de propriétés qui s’affichent lorsque l’utilisateur sélectionne des **Propriétés** dans le menu contextuel de l’icône **courrier électronique** (ou **Internet**). Par exemple, l’application de messagerie Litware ajoute les données **reg \_ SZ** ou **reg \_ développé \_** suivantes pour afficher une feuille de propriétés personnalisée pour l’icône de **courrier électronique** plutôt que sa feuille de propriétés par défaut.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

L’élément de données MUIVerb est construit à partir d’un signe « at » (@), suivi du chemin d’accès complet à la DLL de ressource, d’une virgule, d’un signe moins (-), puis de l’identificateur de ressource de chaîne décimale à afficher. Notez que le chemin d’accès au programme LitMail.exe contient des espaces, donc la chaîne du chemin d’accès est placée entre guillemets.

Une application peut également ajouter des commandes supplémentaires au menu contextuel. Par exemple, l’application de messagerie Litware ajoute une commande **Find** avec les données de **reg \_ SZ** suivantes :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

Le nom de la sous-clé sous l' **interpréteur** de commandes (dans le cas présent, « Find ») est un nom arbitraire et non localisé. Une fois encore, les données MUIVerb contiennent un signe « at » (@) comme premier élément, suivi du chemin d’accès à une DLL de ressource, d’un séparateur de virgule, puis d’un signe moins avant l’identificateur de ressource de chaîne décimale. Par exemple, cette ressource de type chaîne peut être « ouvrir le carnet d’adresses ». Enfin, Notez que la chaîne de ligne de commande contient des espaces, donc elle est placée entre guillemets.

 

 
