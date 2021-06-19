---
description: Découvrez comment utiliser l’argument de navigation dans l’interface utilisateur du shell Windows pour contrôler l’étendue d’une recherche.
title: Argument de navigation (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 543bc90647bbe1daed1a3a6d1f7bc54a4713a8ed
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403602"
---
# <a name="crumb-argument-the-windows-shell"></a>Argument de navigation (shell Windows)

L' `crumb` argument prend en charge les instructions de syntaxe de requête avancée (AQS) complète et est particulièrement utile pour contrôler l’étendue d’une recherche. En plus des instructions AQS, l' `crumb` argument peut accepter un `location` paramètre spécial sur Windows Vista et `kind` les `store` paramètres et sur Windows XP, comme décrit plus loin dans cette rubrique.

Cette rubrique contient les sections suivantes :

-   [Syntaxe de la navigation](#crumb-syntax)
    -   [Exemples généraux](#general-examples)
-   [Utilisation de la navigation avec Vista (emplacement)](#using-crumb-with-vista-location)
    -   [Exemples Vista](#vista-examples)
    -   [Constantes pour les dossiers communs](#constants-for-common-folders)
    -   [Informations sur les arguments](#argument-information)

## <a name="crumb-syntax"></a>Syntaxe de la navigation

La syntaxe de la navigation est la suivante :


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> partie est toute propriété dans le système de propriétés, et le <value> la partie est une valeur valide pour cette propriété. La <label> partie est un alias facultatif pour la propriété qui s’affiche comme un indicateur d’interface utilisateur.

### <a name="general-examples"></a>Exemples généraux


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Utilisation de la navigation avec Vista (emplacement)

Dans le paramètre de navigation, Windows Vista prend en charge la AQS complète et également la `location` propriété, qui a une implémentation spéciale disponible uniquement sur Windows Vista. Vous pouvez utiliser une chaîne AQS ou la `location` propriété dans un seul paramètre de navigation, mais pas les deux. Si le paramètre de navigation inclut AQS, tout le reste dans ce paramètre de navigation est ignoré.

La `location` propriété vous permet de spécifier un chemin d’accès à rechercher. Windows Vista peut contourner l’indexeur et traverser le répertoire directement si l’emplacement se trouve en dehors de la portée de l’analyse de l’indexeur. Par conséquent, ces recherches peuvent être plus lentes que les recherches qui utilisent l’indexeur.

Lorsque vous spécifiez une `location` propriété, deux paramètres supplémentaires sont pris en charge et facultatifs :



| Paramètre | Valeurs                  | Description                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusion | inclure, exclure        | Spécifie si la requête doit inclure ou exclure des éléments de ce chemin d’accès. « Include » est la valeur par défaut. Windows Vista ne prend pas en charge les exclusions sans inclusions. (Voir l’exemple) |
| récursivité | récursif, récursif | Spécifie si la recherche doit recurseiser tous les sous-dossiers à partir de la valeur définie dans l’emplacement :<value>. « Recursive » est la valeur par défaut.                             |



 

Pour étendre une recherche à l’aide du protocole **Search :** , vous disposez de différentes options en fonction de la cible de l’étendue.

Dossier sur un ordinateur local :

-   Utilisez AQS (navigation = dossier : <chemin d’accès encodé URL>)
-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

Dossier sur un ordinateur/réseau distant :

-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

Dossier accessible via un gestionnaire de protocole UNC (Universal Naming Convention) connu :

-   Utilisez AQS (navigation = Store : <UNC protocol handler name> )
-   Use location argument (navigation = Location : <chemin d’accès encodé URL>)

### <a name="vista-examples"></a>Exemples Vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Le premier exemple exécute une recherche de « vacances » en commençant à l' `shell://Personal` emplacement (un raccourci spécial vers le dossier **Mes documents** de l’utilisateur), y compris ce dossier et tous ses sous-dossiers. Consultez le tableau ci-dessous.

Le deuxième exemple exécute une recherche dans C : \\ images, mais pas dans c : \\ images \\ en double.

Le troisième exemple exécute une recherche dans les documents C : \\ , limitée aux fichiers dont la `kind` propriété a la valeur pics.

### <a name="constants-for-common-folders"></a>Constantes pour les dossiers communs

Windows Vista permet l’utilisation de valeurs CSIDL qui fournissent une méthode unique indépendante du système pour identifier les dossiers spéciaux utilisés fréquemment par les applications, mais qui peuvent ne pas avoir le même nom ou emplacement sur un système donné. Par exemple, le dossier système peut être « C : \\ Windows » sur un système et « c : \\ winnt » sur un autre.

Utilisez ces emplacements avec la syntaxe suivante :


```
crumb=location:shell%3a<LocationName>&
```



Le tableau suivant répertorie les valeurs de CSIDL. Pour plus d’informations, consultez [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .



| Nom                        | chaîne de recherche                   | Description                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OUTILS D’ADMINISTRATION        | % 20TOOLS D’ADMINISTRATION          | Répertoire du système de fichiers qui sert de référentiel pour les outils d’administration.                                                                                                            |
| APPDATA                     | APPDATA                         | Répertoire du système de fichiers qui sert de référentiel commun pour les données spécifiques à l’application. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ Application Data.                      |
| CACHE                       | CACHE                           | Répertoire du système de fichiers qui sert de référentiel commun pour les fichiers Internet temporaires. Un chemin d’accès standard est C : \\ Documents and Settings \\ nom d’utilisateur \\ fichiers Internet temporaires.               |
| GRAVAGE DE CD                  | CD% 20BURNING                    | Dossier contenant les données à graver sur CD.                                                                                                                                             |
| OUTILS D’ADMINISTRATION COURANTS | % 20ADMINISTRATIVE% 20TOOLS COURANT | Outils d’administration pour tous les utilisateurs.                                                                                                                                                    |
| APPDATA COMMUN              | % 20APPDATA COURANT                | Données d’application pour tous les utilisateurs. Un chemin d’accès standard est C : \\ Documents and Settings \\ All Users \\ Application Data.                                                                             |
| BUREAU COMMUN              | BUREAU COMMUN                  | Données de bureau Microsoft Windows pour tous les utilisateurs. Dossier virtuel qui est la racine de l’espace de noms.                                                                                        |
| DOCUMENTS COMMUNS            | % 20DOCUMENTS COURANT              | Documents pour tous les utilisateurs. Un chemin d’accès standard est C : \\ Documents and Settings \\ All Users \\ My documents.                                                                                        |
| PROGRAMMES COURANTS             | % 20PROGRAMS COURANT               | Groupes de programmes communs à tous les utilisateurs. Un chemin d’accès standard est C : \\ Documents and Settings \\ All Users \\ Program menu Start \\ Programs.                                                                     |
| MENU DÉMARRER COMMUN           | % 20START% 20MENU COURANT           | Éléments du menu Démarrer communs à tous les utilisateurs. Le chemin d’accès standard est C : \\ Documents and Settings \\ All Users \\ menu Démarrer.                                                                             |
| DÉMARRAGE COURANT              | % 20STARTUP COURANT                | Groupe de programmes de démarrage commun à tous les utilisateurs.                                                                                                                                             |
| MODÈLES COMMUNS            | % 20TEMPLATES COURANT              | Modèles de document communs à tous les utilisateurs.                                                                                                                                                |
| COMMONMUSIC                 | MON% 20MUSIC                      | Mes modèles de dossier de musique communs à tous les utilisateurs.                                                                                                                                         |
| COMMONPICTURES              | MON% 20PICTURES                   | Modèles de dossiers Mes images communs à tous les utilisateurs.                                                                                                                                      |
| COMMONVIDEO                 | MON% 20VIDEO                      | Mes modèles de dossiers vidéo communs à tous les utilisateurs.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | dossier contenant les données de connexion.                                                                                                                                                     |
| DOSSIER DU PANNEAU DE CONFIGURATION        | CONTROLPANELFOLDER              | Dossier virtuel contenant les icônes des applications du panneau de configuration.                                                                                                                    |
| INTERNES                     | INTERNES                         | Répertoire du système de fichiers qui sert de référentiel commun pour les cookies Internet. Un chemin d’accès standard est C : \\ Documents and Settings \\ nom d’utilisateur \\ cookies.                                        |
| BUREAU                     | BUREAU                         | Microsoft Windows Desktop. Dossier virtuel qui est la racine de l’espace de noms.                                                                                                           |
| FAVORIS                   | FAVORIS                       | Répertoire du système de fichiers qui sert de référentiel commun pour les éléments favoris de l’utilisateur. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ favorites.                             |
| POLICE                       | POLICE                           | Dossier virtuel contenant les polices installées. Le chemin d’accès standard est C : \\ Windows \\ polices.                                                                                                       |
| HISTORIQUE                     | HISTORIQUE                         | Répertoire du système de fichiers qui sert de référentiel commun pour les éléments de l’historique Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Dossier qui contient les données Internet.                                                                                                                                                    |
| APPDATA LOCAL               | % 20APPDATA LOCAL                 | Répertoire du système de fichiers qui sert de référentiel de données pour les applications locales (non itinérantes). Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ Local Settings \\ Application Data. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Répertoire de ressources localisé.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Poste de travail : Dossier virtuel contenant tout sur l’ordinateur local : les périphériques de stockage, les imprimantes et le panneau de configuration. Ce dossier peut également contenir des lecteurs réseau mappés.             |
| MA MUSIQUE                    | MON% 20MUSIC                      | Dossier ma musique. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ My documents \\ My Music.                                                                                       |
| MES IMAGES                 | MON% 20PICTURES                   | Dossier Mes images. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ My documents \\ My Pictures.                                                                                 |
| MA VIDÉO                    | MON% 20VIDEO                      | Dossier My Video. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ My documents \\ My Video.                                                                                       |
| Nethotte                     | Nethotte                         | Dossier virtuel représentant la racine de la hiérarchie d’espace de noms de réseau.                                                                                                               |
| DOSSIER EMPLACEMENTS RÉSEAU       | NETWORKDPLACESFOLDER            | Dossier du système de fichiers qui contient les objets de lien qui peuvent exister dans le dossier virtuel Favoris réseau. Il n’est pas identique à nethott, qui représente la racine de l’espace de noms réseau.   |
| LIENS OEM                   | OEM% 20LINKS                     | Dossier contenant des liens vers des sites OEM.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Répertoire du système de fichiers qui sert de référentiel commun pour les documents d’un utilisateur. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ My documents.                                 |
| DOSSIER IMPRIMANTES             | DOSSIER IMPRIMANTES                 | Dossier virtuel contenant les imprimantes installées.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Répertoire du système de fichiers qui contient les objets de lien qui peuvent exister dans le dossier virtuel imprimantes. Un chemin d’accès standard est C : \\ Documents and Settings \\ nom_utilisateur \\ PrintHood.                 |
| PROGRAMMES                    | PROGRAMMES                        | Répertoire du système de fichiers qui contient les groupes de programmes de l’utilisateur (qui sont également des répertoires du système de fichiers). Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ menu Start \\ Programs.  |
| PROFILE                     | PROFILE                         | Dossier du profil de l’utilisateur.                                                                                                                                                                 |
| FICHIERS PROGRAMME               | PROGRAMME% 20FILES                 | Dossier Program Files. Un chemin d’accès standard est C : \\ Program Files.                                                                                                                             |
| FICHIERS DE PROGRAMME COMMUNS        | PROGRAMFILESCOMMON              | Dossier Program Files commun à tous les utilisateurs.                                                                                                                                              |
| PROGRAM FILES COMMON x86    | PROGRAMFILESCOMMONX86           | Dossier Program Files commun à tous les utilisateurs sur les ordinateurs x86.                                                                                                                              |
| FILESx86 du programme            | PROGRAMFILESx86                 | Dossier Program Files sur les ordinateurs x86.                                                                                                                                                  |
| ULTÉRIEURE                      | ULTÉRIEURE                          | Répertoire du système de fichiers qui contient les documents les plus récemment utilisés par l’utilisateur. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ récent.                                           |
| DOSSIER CORBEILLE          | RECYCLEBINFOLDER                | Dossier virtuel contenant les objets de la corbeille de l’utilisateur.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Répertoire de ressources.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Répertoire du système de fichiers qui contient les éléments de menu Envoyer vers. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ SendTo.                                                                |
| MENU DÉMARRER                  | DÉMARRER% 20MENU                    | Répertoire du système de fichiers contenant les éléments du menu Démarrer. Un chemin d’accès standard est C : \\ Documents and Settings \\ UserName \\ menu Démarrer.                                                                 |
| DU                     | DU                         | Répertoire du système de fichiers qui correspond au groupe de programmes de démarrage de l’utilisateur.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Dossier système sur les ordinateurs x86.                                                                                                                                                         |
| TEMPLATES                   | TEMPLATES                       | Répertoire du système de fichiers qui sert de référentiel commun pour les modèles de document.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Dossier système. Un chemin d’accès standard est C : \\ \\ système Windows.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Répertoire Windows ou SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informations sur les arguments



|                              | Valeur                                   |
|------------------------------|-----------------------------------------|
| **Système d’exploitation minimal** | Windows Vista Service Pack 1 (SP1) |



 

 

 



