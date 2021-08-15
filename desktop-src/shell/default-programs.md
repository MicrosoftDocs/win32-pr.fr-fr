---
description: Utilisez les programmes par défaut pour définir l’expérience utilisateur par défaut.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programmes par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861356"
---
# <a name="default-programs"></a>Programmes par défaut

Utilisez les **programmes par défaut** pour définir l’expérience utilisateur par défaut. Les utilisateurs peuvent accéder aux **programmes par défaut** à partir du panneau de configuration ou directement à partir du menu **Démarrer** . l’outil [définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) , l’expérience des valeurs par défaut principales pour les utilisateurs dans Windows XP, est désormais un composant des **programmes par défaut**.

> [!IMPORTANT]
> Cette rubrique ne s’applique pas à Windows 10. La façon dont les associations de fichiers par défaut fonctionnent dans Windows 10. pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Quand un utilisateur définit les paramètres par défaut du programme à l’aide de **programmes par défaut**, le paramètre par défaut s’applique uniquement à cet utilisateur et non aux autres utilisateurs qui peuvent utiliser le même ordinateur. les **programmes par défaut** fournissent un ensemble d’api (déconseillées dans Windows 8) qui permettent aux éditeurs de logiciels indépendants d’inclure leurs programmes ou applications dans le système par défaut. L’ensemble d’API permet également aux éditeurs de logiciels indépendants de mieux gérer leur état par défaut.

Cette rubrique est organisée comme suit :

-   [Présentation des programmes par défaut et de l’ensemble des API associées](#introduction-to-default-programs-and-its-related-api-set)
-   [Inscription d’une application pour une utilisation avec les programmes par défaut](#registering-an-application-for-use-with-default-programs)
    -   [ProgID](#progids)
    -   [Sous-clé d’inscription et descriptions de valeur](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Exemple d’inscription complète](#full-registration-example)
-   [Devenir le navigateur par défaut](#becoming-the-default-browser)
-   [Interface utilisateur des programmes par défaut](#default-programs-ui)
-   [Meilleures pratiques pour l’utilisation des programmes par défaut](#best-practices-for-using-default-programs)
    -   [Pendant l’installation](#during-installation)
    -   [Après l’installation](#after-installation)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Présentation des programmes par défaut et de l’ensemble des API associées

Les **programmes par défaut** sont principalement conçus pour les applications qui utilisent des types de fichiers standard, tels que des fichiers .mp3 ou .jpg ou des protocoles standard, tels que http ou mailto. Les applications qui utilisent leurs propres protocoles et associations de fichiers propriétaires n’utilisent généralement pas les fonctionnalités des **programmes par défaut** .

Une fois que vous avez inscrit une application pour la fonctionnalité **programmes par défaut** , les options et fonctionnalités suivantes sont disponibles à l’aide de l’API Set :

-   Restaure toutes les valeurs par défaut enregistrées pour une application. Déconseillé pour Windows 8.
-   Restaure une valeur par défaut enregistrée pour une application. Déconseillé pour Windows 8.
-   Interrogez le propriétaire d’une valeur par défaut spécifique dans un appel unique au lieu de rechercher dans le registre. Vous pouvez rechercher la valeur par défaut d’une association de fichier, d’un protocole ou d’un verbe canonique du menu **Démarrer** .
-   Lancer une interface utilisateur pour une application spécifique où un utilisateur peut définir des valeurs par défaut individuelles.
-   Supprimer toutes les associations par utilisateur.

Les **programmes par défaut** fournissent également une interface utilisateur qui vous permet d’inscrire une application afin de fournir des informations supplémentaires à l’utilisateur. Par exemple, une application signée numériquement peut inclure une URL vers la page d’hébergement du fabricant.

l’utilisation de l’ensemble d’API associé peut permettre à une application de fonctionner correctement sous la fonctionnalité de contrôle de compte d’utilisateur (UAC, user account control) introduite dans Windows Vista. Sous UAC, un administrateur apparaît comme utilisateur standard dans le système, afin que l’administrateur ne puisse généralement pas écrire dans la sous-arborescence de l' **\_ \_ ordinateur local HKEY** . Cette restriction est une fonctionnalité de sécurité qui empêche un processus d’agir en tant qu’administrateur sans la connaissance de l’administrateur.

L’installation d’un programme par un utilisateur s’effectue généralement sous la forme d’un processus élevé. Toutefois, les tentatives effectuées par une application pour modifier les comportements d’association par défaut au niveau de l’ordinateur après l’installation seront infructueuses. Au lieu de cela, les valeurs par défaut doivent être inscrites sur un niveau par utilisateur, ce qui empêche plusieurs utilisateurs de remplacer les valeurs par défaut des autres.

La structure hiérarchique du Registre pour les associations de fichiers et de protocoles donne la priorité aux valeurs par défaut par utilisateur par rapport aux valeurs par défaut au niveau de l’ordinateur. Certaines applications incluent des points dans leur code qui élèvent temporairement leurs droits lorsqu’ils revendiquent les valeurs par défaut inscrites dans **HKEY \_ local \_ machine**. Ces applications peuvent présenter des résultats inattendus si une autre application est déjà inscrite en tant que valeur par défaut par utilisateur. L’utilisation de **programmes par défaut** empêche cette ambiguïté et garantit des résultats attendus pour chaque utilisateur.

## <a name="registering-an-application-for-use-with-default-programs"></a>Inscription d’une application pour une utilisation avec les programmes par défaut

Cette section présente les sous-clés et les valeurs de Registre nécessaires pour inscrire une application avec des **programmes par défaut**. Elle contient un exemple complet.

Cette section contient les rubriques suivantes :

-   [ProgID](#progids)
-   [Sous-clé d’inscription et descriptions de valeur](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Exemple d’inscription complète](#full-registration-example)

Les **programmes par défaut** requièrent que chaque application enregistre explicitement les associations de fichiers, les associations MIME et les protocoles pour lesquels l’application doit être listée comme une valeur par défaut possible. Vous inscrivez les associations à l’aide des éléments de registre suivants, qui sont expliqués en détail plus loin dans cette rubrique, sous la sous [-clé d’inscription et les descriptions de valeurs](#registration-subkey-and-value-descriptions):

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

L’exemple suivant montre les entrées de Registre pour un navigateur contoso fictif appelé WebBrowser :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>ProgID

Une application doit fournir un [ProgID](fa-progids.md)spécifique. Veillez à inclure toutes les informations qui sont généralement écrites dans la sous-clé générique par défaut pour l’extension. Par exemple, le lecteur multimédia fiction Litware fournit la sous-clé de laLitwarePlayer11.AssocFile.MP3de classes de logiciels **HKEY \_ local \_ machine** propre à l’application \\  \\  \\ **** . Cette sous-clé contient toutes les informations contenues dans la sous-clé par défaut générique **HKEY \_ local \_ machine** classes de \\ **logiciels** \\  \\ **.mp3** plus toutes les informations supplémentaires que l’application doit inscrire. Cela garantit que si l’utilisateur restaure l’Association de .mp3 à Litware Player, les informations de Litware Player sont intactes et n’ont pas été remplacées par une autre application. (Le remplacement peut se produire si la sous-clé par défaut est la seule source de ces informations.)

Lorsque vous mappez un ProgID à un protocole ou une extension de nom de fichier, une application peut mapper un-à-un ou un-à-plusieurs. Dans l’exemple Contoso, ContosoHTML pointe vers un ProgID unique qui fournit des informations ShellExecute pour les extensions .htm, .html,. shtml,. XHT et. XHTML. Comme il existe un ProgID différent pour chaque protocole, lorsque vous utilisez des protocoles, vous permettez à chaque protocole d’avoir sa propre chaîne d’exécution.

Lorsque votre type MIME peut être affiché inline dans un navigateur, le ProgID du type MIME doit contenir la sous-clé **CLSID** qui utilise l’identificateur de classe (CLSID) de l’application correspondante. Ce CLSID est utilisé dans une recherche par rapport au CLSID dans la base de données MIME qui est stockée dans le **\_ \_** \\  \\  \\  \\ type **de contenu de la base de données de la base de données MIME de** la classe de \\ l’ordinateur local. Si votre type MIME n’est pas destiné à être affiché inline dans un navigateur, cette étape peut être omise.

### <a name="registration-subkey-and-value-descriptions"></a>Sous-clé d’inscription et descriptions de valeur

Cette section décrit les sous-clés et les valeurs de Registre individuelles utilisées pour l’inscription d’une application avec les **programmes par défaut**, comme illustré précédemment.

### <a name="capabilities"></a>Fonctions

La sous-clé **Capabilities** contient toutes les informations sur les **programmes par défaut** pour une application spécifique. L’espace réservé% ApplicationCapabilityPath% fait référence au chemin d’accès du registre de **HKEY \_ Current \_ User** ou **HKEY \_ local \_ machine** à la sous-clé **Capabilities** de l’application. Cette sous-clé contient les valeurs significatives indiquées dans le tableau suivant.



| Valeur                  | Type                       | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ ou reg \_ développé \_ SZ | **Requis**. Pour permettre à un utilisateur d’effectuer un choix d’affectation par défaut informé, une application doit fournir une chaîne décrivant les fonctionnalités de l’application. Bien que l’exemple Contoso précédent affecte la description directement à la valeur ApplicationDescription, les applications fournissent généralement la description en tant que ressource incorporée dans un fichier .dll pour faciliter la localisation. Si ApplicationDescription n’est pas fourni, l’application n’apparaît pas dans les listes d’interface utilisateur des programmes potentiels par défaut.                                                            |
| ApplicationName        | REG \_ SZ ou reg \_ développé \_ SZ | **Facultatif.** Nom sous lequel le programme apparaît dans l’interface utilisateur des programmes par défaut. Si ces données ne sont pas fournies par l’application, le nom du programme exécutable associé au premier ProgID enregistré pour l’application est utilisé dans l’interface utilisateur. ApplicationName doit toujours correspondre au nom enregistré sous [RegisteredApplications](#registeredapplications). Vous pouvez utiliser ApplicationName si vous souhaitez que différents types d’application, tels qu’un navigateur et un client de messagerie, pointent vers le même fichier exécutable lorsqu’ils apparaissent sous la forme de noms différents.<br/> |
| Hidden                 | \_valeur DWORD reg                 | **Facultatif.** Définissez cette valeur sur 1 pour supprimer l’application de la liste des programmes dans la boîte de dialogue **définir vos programmes par défaut** . Si cette valeur est égale à 0 ou absente, l’application s’affiche normalement dans la liste.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

La sous-clé **FileAssociations** contient des associations de fichiers spécifiques revendiquées par l’application. Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque extension. Les associations pointent vers un ProgID spécifique à l’application au lieu d’un ProgID générique. Toutefois, il n’est pas nécessaire que toutes les associations pointent vers le même ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

La sous-clé **MIMEAssociations** contient des types MIME spécifiques revendiqués par l’application. Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque type MIME. Le nom de la valeur de chaque type MIME doit correspondre exactement au nom MIME stocké dans la base de données MIME. La valeur doit également être assignée à un ProgID spécifique à l’application qui contient le CLSID correspondant de l’application.

### <a name="startmenu"></a>Restauré

La sous-clé **restauré** est associée à l’adresse **Internet** et aux entrées de **courrier électronique** attribuables par l’utilisateur dans le menu **Démarrer** . Une application doit s’inscrire séparément en tant que contendeur pour ces entrées. Pour plus d’informations, consultez [inscription de programmes avec des types de clients](reg-middleware-apps.md).

> [!Note]  
> à partir de Windows 7, il n’y a plus d’entrées **Internet** et de **messagerie électronique** dans le menu **démarrer** . les données de registre associées à l’entrée de **courrier électronique** sont toujours utilisées pour le client MAPI par défaut, mais les données de registre associées à l’entrée **Internet** ne sont pas utilisées par Windows du tout.

 

En associant l’inscription du menu **Démarrer** à une application avec son inscription de **programmes par défaut** , l’application apparaît comme une valeur par défaut potentielle dans l’interface utilisateur **définir les associations** . Si l’utilisateur a choisi l’application comme valeur par défaut, puis choisit de restaurer toutes les valeurs par défaut de l’application ultérieurement, l’application est restaurée à sa position de menu **Démarrer** pour cet utilisateur. Pour plus d’informations et une illustration, consultez la section de l' [interface utilisateur des programmes par défaut](#default-programs-ui) plus loin dans cette rubrique.

La sous-clé **restauré** comporte deux entrées : StartMenuInternet et mail, qui correspondent aux positions canoniques de **messagerie** et **Internet** dans le menu **Démarrer** . Une application affecte StartMenuInternet ou mail une valeur égale au nom de la sous-clé inscrite de l’application sous **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** ou **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** (comme décrit dans [inscription de programmes avec des types de client](reg-middleware-apps.md)).

Dans le cas de la position canonique par **courrier électronique** dans le menu **Démarrer** , elle représente le client MAPI par défaut et est donc supposée être en mesure de transmettre des appels MAPI. sous Windows 7, bien qu’il n’y ait plus de position canonique par **courrier électronique** dans le menu **démarrer** , cette sous-clé continue à être utilisée pour le client MAPI par défaut. Une application revendiquant la valeur par défaut du courrier doit s’inscrire en tant que gestionnaire MAPI sous la sous-clé suivante :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Si un client de messagerie ne peut pas prendre en charge MAPI mais souhaite toujours faire face à la position canonique de **messagerie** du menu **Démarrer** , il peut inscrire une ligne de commande sous la sous-clé suivante :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

En outre, sous **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** \\ *CanonicalName* , ajoutez une valeur par défaut avec le nom de l’application.

Ces entrées permettent à l’application d’être lancée à partir de la position du **message électronique** du menu **Démarrer** . Notez que les appels MAPI sont toujours effectués à l’application et passent par le gestionnaire MAPI précédent, ou échouent si aucun gestionnaire MAPI n’a été défini. Pour plus d’informations, consultez [inscription de programmes avec des types de clients](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

La sous-clé **UrlAssociations** contient les protocoles d’URL spécifiques revendiqués par l’application. Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque protocole. Chaque protocole doit pointer vers un ProgID spécifique à l’application et non vers un ProgID générique. Comme mentionné dans l’exemple de contoso, vous pouvez utiliser un ProgID différent pour chaque protocole afin que chacun ait sa propre chaîne d’exécution.

### <a name="registeredapplications"></a>RegisteredApplications

La sous-clé complète de **RegisteredApplications** est :

**HKEY \_ \_** \\  \\ **RegisteredApplications** logiciel de l’ordinateur local

Cette sous-clé fournit au système d’exploitation l’emplacement du registre des informations sur les **programmes par défaut** de l’application. L’emplacement est stocké sous la forme d’une valeur dont le nom doit correspondre au nom de l’application.

### <a name="full-registration-example"></a>Exemple d’inscription complète

Cet exemple montre les sous-clés et les valeurs utilisées lors de l’inscription du lecteur multimédia Litware-fiction. L’exemple comprend les entrées ProgID afin d’illustrer la façon dont elles s’ajustent.

La sous-clé suivante montre le ProgID spécifique à l’application pour le .mp3 type MIME :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Ensuite, il s’agit du ProgID propre à l’application qui associe le programme Litware à l’extension de nom de fichier .mp3.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Les entrées suivantes affichent le ProgID combiné pour l' .mpeg type MIME et l’extension de nom de fichier.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

Les entrées suivantes inscrivent le programme Litware dans les **programmes par défaut** et utilisent les ProgID précédemment enregistrés

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

Enfin, cet exemple inscrit l’emplacement de l’inscription des **programmes Litware par défaut** .

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Devenir le navigateur par défaut

L’inscription du navigateur doit suivre les meilleures pratiques décrites dans cette rubrique. lors de l’installation du navigateur, Windows pouvez présenter à l’utilisateur une notification système par l’intermédiaire de laquelle l’utilisateur peut sélectionner le navigateur comme système par défaut. Cette notification s’affiche lorsque ces conditions sont remplies :

-   le programme d’installation du navigateur appelle [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) à l’aide de l’indicateur **SHCNE \_ ASSOCCHANGED** pour indiquer Windows que de nouveaux gestionnaires de protocole ont été inscrits.
-   Windows détecte qu’une ou plusieurs nouvelles applications sont inscrites pour gérer à la fois les protocoles http://et https://, et l’utilisateur n’a pas encore été notifié. En d’autres termes, aucun des éléments suivants n’a été présenté à l’utilisateur : une notification système publiant l’application, un menu volant OpenWith contenant l’application ou la page définir les paramètres par défaut des utilisateurs (SUD) de l’application.

L’exemple suivant montre le code d’inscription recommandé que le programme d’installation du navigateur doit exécuter après avoir écrit ses clés de registre.

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) informe tout d’abord le système que de nouveaux choix d’association sont disponibles. L’appel **SHChangeNotify** est requis pour garantir le bon fonctionnement des paramètres système par défaut.

Une instruction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) autorise ensuite les processus système à gérer la notification.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Si l’utilisateur ignore ou ignore la notification ou le menu volant qui en résulte sans effectuer de nouvelle sélection de navigateur par défaut, le navigateur par défaut reste inchangé. Notez que l’utilisateur peut également modifier le navigateur par défaut à tout moment à l’aide d’autres mécanismes, y compris définir les paramètres par défaut de l’utilisateur dans le panneau de configuration.

## <a name="default-programs-ui"></a>Interface utilisateur des programmes par défaut

Les illustrations de cette section illustrent l’interface utilisateur des **programmes par défaut** , telle qu’elle est affichée par l’utilisateur.

L’illustration suivante montre la fenêtre principale **programmes par défaut** du panneau de configuration.

![capture d’écran de la page d’entrée programmes par défaut](images/defaultprogramsmain.png)

Quand un utilisateur choisit l’option **définir vos programmes par défaut** , la fenêtre suivante s’affiche. Les utilisateurs peuvent utiliser cette page pour affecter un programme par défaut pour tous les types de fichiers et protocoles pour lesquels le programme est une option par défaut. Comme indiqué dans l’illustration suivante, tous les programmes [inscrits](#registering-an-application-for-use-with-default-programs) et l’icône de programme s’affichent dans la zone **programmes** sur la gauche.

![capture d’écran de la page définir vos programmes par défaut](images/setyourdefaultprograms.png)

Lorsque l’utilisateur sélectionne un programme dans la liste, l’icône et le fournisseur du programme s’affichent. Si l’URL est incorporée dans le certificat signé numériquement, le programme peut également afficher une URL. Les programmes qui ne sont pas signés numériquement ne peuvent pas afficher une URL.

Le texte descriptif, qui est fourni par le programme lors de l’inscription, est également affiché. Ce texte est obligatoire. Sous la zone Description, vous pouvez indiquer le nombre de valeurs par défaut actuellement affectées par le programme à partir du nombre complet qu’il est inscrit pour gérer.

Pour affecter ou restaurer un programme comme valeur par défaut pour tous les fichiers et protocoles pour lesquels il est inscrit, l’utilisateur clique sur l’option **définir ce programme comme programme par défaut** .

Pour assigner des types de fichiers et des protocoles individuels à un programme, l’utilisateur clique sur l’option **choisir les paramètres par défaut pour ce programme** , qui affiche une fenêtre **définir les associations pour un programme** comme celle de l’illustration suivante.

> [!Note]  
> Nous vous recommandons d’appeler les **associations Set pour un programme** à l’aide de [**IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![capture d’écran de la page définir les associations pour un programme](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Meilleures pratiques pour l’utilisation des programmes par défaut

Cette section présente les meilleures pratiques pour l’utilisation des **programmes par défaut** lorsque vous inscrivez des applications. Il offre également des suggestions de conception pour la création d’une application qui fournit aux utilisateurs des fonctionnalités optimales de **programmes par défaut** .

### <a name="during-installation"></a>Pendant l’installation

en plus des procédures d’installation normalement recommandées sous Windows XP, une application Windows Vista ou version ultérieure doit s’inscrire auprès de la fonctionnalité **programmes par défaut** pour tirer parti de ses fonctionnalités.

Procédez comme suit lors de l’installation. les étapes 1-3 correspondent aux étapes utilisées dans Windows XP ; l’étape 4 est une nouveauté de Windows Vista.

1.  Installez les fichiers binaires nécessaires.
2.  Écrivez les ProgID sur \_ la \_ machine locale HKEY. Notez que les applications doivent créer des ProgID spécifiques à l’application pour leurs associations.
3.  Inscrivez l’application avec les **programmes par défaut** comme expliqué précédemment dans [inscription d’une application pour une utilisation avec les programmes par défaut](#registering-an-application-for-use-with-default-programs).

### <a name="after-installation"></a>Après l’installation

Cette section explique comment l’invite de l’application doit d’abord présenter ses options par défaut à chaque utilisateur. Il explique également comment une application peut surveiller son état par défaut pour ses associations et protocoles possibles.

### <a name="first-run-experiences"></a>Expériences de première exécution

Lorsque l’application est exécutée par un utilisateur pour la première fois, il est recommandé que l’application affiche l’interface utilisateur pour l’utilisateur qui comprend généralement les deux choix suivants :

-   Acceptez les paramètres d’application par défaut. Cette option est activée par défaut.
-   Personnaliser les paramètres d’application par défaut.

avant de Windows 8, si l’utilisateur accepte les paramètres par défaut, votre application appelle [**IApplicationAssociationRegistration :: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), qui convertit toutes les associations au niveau de l’ordinateur déclarées lors de l’installation en paramètres par utilisateur pour cet utilisateur.

Si l’utilisateur décide de personnaliser les paramètres, votre application appelle [**IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) pour afficher l’interface utilisateur d’association de fichiers. L’illustration suivante montre cette fenêtre pour le lecteur multimédia Litware-fiction.

![capture d’écran de la page définir des associations pour un programme pour Litware](images/setassociationsforaprogramforlitware.png)

La fenêtre Association de fichiers affiche les valeurs par défaut inscrites par l’application et indique également la valeur par défaut actuelle pour d’autres extensions et protocoles. Une fois que l’utilisateur a fini de personnaliser ses valeurs par défaut, il clique sur le bouton **Enregistrer** pour valider les modifications. Si l’utilisateur clique sur **Annuler**, la fenêtre se ferme sans enregistrer les modifications.

Vous devez utiliser cette interface utilisateur pour vos applications au lieu de créer les vôtres. En procédant ainsi, vous enregistrez les ressources qui ont été préalablement requises pour développer l’interface utilisateur d’association de fichiers. Vous garantissez également que les associations sont correctement enregistrées.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Définir une application pour vérifier s’il s’agit de la valeur par défaut

> [!Note]  
> Cette fonction n’est plus prise en charge à partir de Windows 8.

 

En règle générale, les applications vérifient si elles sont définies comme valeurs par défaut lorsqu’elles sont exécutées. Définissez vos applications pour effectuer cette vérification en appelant [**IApplicationAssociationRegistration :: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) ou [**IApplicationAssociationRegistration :: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Si l’application détermine qu’il ne s’agit pas de la valeur par défaut, elle peut présenter une interface utilisateur qui demande à l’utilisateur s’il faut accepter la situation actuelle ou pour que l’application soit la valeur par défaut. Incluez toujours une case à cocher dans cette interface utilisateur qui est sélectionnée par défaut et qui présente l’option ne pas être à nouveau demandée.

> [!Note]  
> Le choix de la valeur par défaut doit être piloté par l’utilisateur. Une application ne doit jamais réclamer une valeur par défaut sans demander à l’utilisateur.

 

L’illustration suivante montre un exemple de boîte de dialogue.

![capture d’écran d’un exemple de boîte de dialogue](images/notthedefaultui.png)

## <a name="additional-resources"></a>Ressources supplémentaires

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les associations de fichiers](fa-best-practices.md)
</dt> <dt>

[Exemple de scénario d’association de fichiers](fa-sample-scenarios.md)
</dt> <dt>

[instructions pour la gestion des Applications par défaut dans Windows Vista et versions ultérieures](vista-managing-defaults.md)
</dt> <dt>

[Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
