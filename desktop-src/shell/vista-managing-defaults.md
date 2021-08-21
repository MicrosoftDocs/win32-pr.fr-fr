---
description: cette rubrique fournit aux éditeurs de logiciels indépendants un guide rapide sur les étapes nécessaires pour inscrire et gérer les valeurs par défaut des applications dans Windows Vista et versions ultérieures. Des liens sont fournis vers des articles plus détaillés sur la rubrique de chaque section.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Gestion des applications par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970034b11e497ac79faafaef352faab1ba56e0c45fee664e576e386f70ef95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675378"
---
# <a name="managing-default-applications"></a>Gestion des applications par défaut

la fonctionnalité **définir l’accès aux programmes et les paramètres par défaut** de l’ordinateur (SPAD) a été ajoutée à Windows XP et versions ultérieures de Windows pour gérer les paramètres par défaut des ordinateurs. en plus de la fonction SPAD, Windows Vista a introduit le concept d’applications par défaut par utilisateur et l’élément **programmes par défaut** dans le panneau de configuration.

> [!IMPORTANT]
> Cette rubrique ne s’applique pas à Windows 10. La façon dont les associations de fichiers par défaut fonctionnent dans Windows 10. pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Les paramètres par défaut par utilisateur sont spécifiques à un compte d’utilisateur individuel sur le système. Si les paramètres par défaut par utilisateur sont présents, ils ont priorité sur les valeurs par défaut correspondant à chaque ordinateur pour ce compte. à partir de Windows 8, le système d’extensibilité pour le type de fichier et les valeurs par défaut du protocole est strictement par utilisateur et les valeurs par défaut par ordinateur sont ignorées. SPAD est également modifié dans Windows 8 pour définir les valeurs par défaut par utilisateur.

-   sur les systèmes exécutant des versions de Windows antérieures à Windows 8, un compte d’utilisateur nouvellement créé reçoit les valeurs par défaut par ordinateur jusqu’à ce que les valeurs par défaut par utilisateur soient établies. dans Windows Vista et versions ultérieures, les utilisateurs peuvent utiliser l’élément **programmes par défaut** dans le panneau de configuration pour définir ou modifier leurs valeurs par défaut par utilisateur. En outre, lorsqu’une application est exécutée pour la première fois, les valeurs par défaut par utilisateur peuvent être définies à l’aide des instructions qui suivent dans la section [première exécution et valeurs par défaut](#application-first-run-and-defaults) de l’application.
-   sur les systèmes exécutant Windows 8, un compte d’utilisateur nouvellement créé s’appuie sur les valeurs par défaut par utilisateur à partir du début et le paramètre de ces valeurs par défaut lors de la première exécution, comme expliqué dans la [première exécution de l’Application, et la section valeurs par défaut](#application-first-run-and-defaults) n’est plus prise en charge.

une application doit s’inscrire à la fois avec SPAD et avec la fonctionnalité programmes par défaut proposée comme programme par défaut dans Windows Vista et versions ultérieures.

cette rubrique fournit aux éditeurs de logiciels indépendants un guide rapide sur les étapes nécessaires pour inscrire et gérer les valeurs par défaut des applications dans Windows Vista et versions ultérieures. Des liens sont fournis vers des articles plus détaillés sur la rubrique de chaque section.

-   [Élément programmes par défaut dans le panneau de configuration](#default-programs-item-in-control-panel)
-   [Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur](#set-program-access-and-computer-defaults)
    -   [Définition des valeurs par défaut dans SPAD](#setting-defaults-in-spad)
    -   [Masquer l’accès dans SPAD](#hide-access-in-spad)
-   [Inscription pour les points d’entrée de l’application](#registering-for-application-entry-points)
    -   [Ouvrir avec](#open-with)
    -   [Menu Démarrer et barre lancement rapide](#start-menu-and-quick-launch-bar)
-   [Installation et paramètres par défaut de l’application](#application-installation-and-defaults)
-   [Mises à niveau et valeurs par défaut de l’application](#application-upgrades-and-defaults)
-   [Première exécution de l’application et valeurs par défaut](#application-first-run-and-defaults)
-   [Vérification des valeurs par défaut et demande de consentement de l’utilisateur](#verifying-defaults-and-asking-for-user-consent)
-   [Astuces de compatibilité des applications](#application-compatibility-tips)
    -   [Éviter le déclenchement de la virtualisation Per-User](#avoid-triggering-per-user-virtualization)
    -   [Éviter les avertissements ou les blocs AppCompat de l’Assistant Compatibilité des programmes](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [prise en charge des Versions précédentes du système d’exploitation Windows](#support-for-previous-windows-operating-system-versions)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Élément programmes par défaut dans le panneau de configuration

les **programmes par défaut** sont une fonctionnalité introduite dans Windows Vista, accessible directement à partir du menu **démarrer** et du panneau de configuration. Il fournit une nouvelle infrastructure qui fonctionne avec un privilège d’utilisateur standard (non élevé) et est conçu pour permettre aux utilisateurs et aux applications de gérer les valeurs par défaut par utilisateur. Pour les utilisateurs, les programmes par défaut offrent un moyen unifié et facilement accessible pour gérer les valeurs par défaut, les associations de fichiers et les paramètres d’exécution automatique sur toutes les applications du système. Pour les applications, l’utilisation de l’étendue par utilisateur fournie par les API des programmes par défaut offre les avantages suivants :

-   **Aucune élévation**

    Une application n’a pas besoin d’élever ses privilèges pour revendiquer les valeurs par défaut.

-   **Bonne citoyenneté**

    Sur un ordinateur à plusieurs utilisateurs, chaque utilisateur peut sélectionner des applications par défaut différentes.

-   **Gestion par défaut**

    Les API des programmes par défaut offrent un mécanisme fiable et cohérent pour la vérification automatique de l’État par défaut et la récupération des paramètres perdus sans avoir recours à l’écriture directe dans le registre. toutefois, à partir de Windows 8, nous déconseillons que les applications interrogent l’état par défaut, car une application ne peut plus changer les paramètres par défaut ; ces modifications ne peuvent être effectuées que par l’utilisateur.

Pour permettre à votre application de gérer efficacement les valeurs par défaut, vous devez inscrire votre application comme programme par défaut potentiel. Pour plus d’informations sur l’inscription et l’utilisation des API des programmes par défaut, consultez [programmes par défaut](default-programs.md).

Les programmes par défaut proposent également les deux fonctionnalités suivantes :

-   **Interface utilisateur par défaut réutilisable**

    L’interface utilisateur des paramètres par défaut du programme (**définir vos programmes par défaut**) et les associations de fichiers (**associer un type de fichier ou un protocole à un programme**) peuvent être réutilisées et appelées à partir d’une application. Cela permet aux applications de fournir une expérience utilisateur standard pour la gestion des valeurs par défaut et évite aux éditeurs de logiciels indépendants d’avoir à développer une interface utilisateur personnalisée ou équivalente.

-   **Inclusion d’URL et d’informations marketing**

    Dans le cadre de la page **définir vos programmes par défaut** de l’élément **programmes par défaut** du panneau de configuration, une application peut fournir des informations de marketing et un lien vers le site Web du fournisseur. Cette URL est dérivée du certificat Authenticode avec lequel l’application a été signée. Cela empêche toute utilisation abusive et le remplacement non autorisé de ce lien. si une application possède un certificat Authenticode qui inclut une url incorporée, Windows interface utilisateur affiche cette url incorporée. Les éditeurs de logiciels indépendants doivent tirer parti de cette fonctionnalité pour diriger les utilisateurs vers leur site Web pour les mises à jour et autres téléchargements.

## <a name="set-program-access-and-computer-defaults"></a>Définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur

**Définir l’accès aux programmes et les valeurs par défaut de l’ordinateur** (SPAD) permet aux administrateurs de gérer les valeurs par défaut à l’ordinateur qui sont héritées par tous les nouveaux utilisateurs de cet ordinateur. avant de Windows 8, la fonctionnalité SPAD permettait également aux administrateurs de réparer les associations de fichiers si les programmes ont été supprimés du système. toutefois, à partir de Windows 8, SPAD affecte uniquement les valeurs par défaut spécifiques à l’utilisateur.

Pour plus d’informations sur l’inscription d’une application dans SPAD, consultez [utilisation de l’option définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) et [inscription de programmes avec des types de clients](reg-middleware-apps.md). Des modifications spécifiques et de nouvelles recommandations sont présentées dans les sections qui suivent.

### <a name="setting-defaults-in-spad"></a>Définition des valeurs par défaut dans SPAD

Les valeurs par défaut par utilisateur remplacent les valeurs par défaut par ordinateur.

-   **avant Windows 8**: les valeurs par défaut définies dans SPAD (qui sont par ordinateur) ne sont pas visibles par les utilisateurs si les valeurs par défaut correspondantes par utilisateur sont définies. Si un utilisateur n’a pas défini de valeur par défaut par utilisateur, le système utilise la valeur par défaut de l’ordinateur correspondant. Les nouveaux comptes d’utilisateur sur un ordinateur héritent initialement des paramètres par défaut de l’ordinateur. La première fois qu’un utilisateur exécute une application, l’application doit inviter l’utilisateur à affecter ses valeurs par défaut par utilisateur. Consultez [première exécution de l’application et valeurs par défaut](#application-first-run-and-defaults).
-   **à partir de Windows 8**: toutes les valeurs par défaut sont par utilisateur et tout paramètre par défaut par ordinateur est ignoré. Les applications ne peuvent plus définir de choix par défaut, de sorte qu’elles ne peuvent pas guider l’utilisateur via l’affectation de ces valeurs par défaut.

quand une application pré-Windows 8 implémente la **valeur par défaut** dans SPAD, ces instructions doivent être suivies :

-   Les applications doivent uniquement revendiquer les paramètres par défaut au niveau de l’ordinateur par le biais de SPAD.
-   Les applications ne doivent *pas* réclamer les valeurs par défaut par utilisateur par le biais de SPAD.

quand une application Windows 8 implémente **Set comme valeur par défaut** dans SPAD, elle doit inscrire ses types de fichiers et protocoles dans les [programmes par défaut](default-programs.md), en utilisant le même nom d’application que celui utilisé dans spad. Cela permet à une modification dans SPAD de refléter comme une modification de l’entrée programmes par défaut correspondante pour l’utilisateur actuel.

### <a name="hide-access-in-spad"></a>Masquer l’accès dans SPAD

L’option Hide Access pour chaque valeur par défaut possible dans SPAD est accessible de deux manières :

-   Choisissez la catégorie **non Microsoft** des valeurs par défaut, qui supprime l’accès à toutes les valeurs par défaut de Microsoft.
-   Choisissez la catégorie **personnalisée** et désactivez la case à cocher **activer l’accès à ce programme** .

Auparavant, l’une de ces actions supprimait tous les points d’entrée des applications appropriées sur le système. Des instructions spécifiques pour cette situation indiquent comment supprimer des raccourcis et des icônes à partir des emplacements suivants :

-   Bureau
-   Menu Démarrer
-   barre lancement rapide (Windows Vista et versions antérieures uniquement)
-   Zone Notifications
-   Menus contextuels
-   Bande de tâches du dossier

Les fournisseurs sont encouragés à implémenter ces instructions dans la fonction de rappel d’accès de masquage de l’application.

### <a name="alternate-hide-access-method-in-spad"></a>Autre méthode d’accès Masquer dans SPAD

Pour certaines applications héritées, une implémentation complète de l’accès masqué peut ne pas être pratique. Une autre méthode qui atteint le même effet, mais qui n’est pas facile à réversible par l’utilisateur, consiste à désinstaller l’application. L’exemple suivant montre un exemple de comportement et de code pour implémenter cela.

L’expérience utilisateur recommandée pour cette solution est la suivante :

-   Quand l’utilisateur désactive la case **activer l’accès à ce programme** dans SPAD, l’interface utilisateur suivante est présentée.

    ![boîte de dialogue Vista sur le masquage de l’accès au programme](images/hideaccessvista.png)

-   Quand l’utilisateur clique sur **OK**, l’élément **programmes et fonctionnalités** du panneau de configuration s’affiche pour permettre à l’utilisateur de désinstaller l’application.
-   Windows Les utilisateurs XP doivent être affichés dans la boîte de dialogue suivante.

    ![boîte de dialogue Windows XP sur le masquage de l’accès au programme](images/hideaccessxp.png)

-   lorsque l’utilisateur Windows XP clique sur **OK**, l’élément **ajout/suppression de programmes** du panneau de configuration s’affiche pour permettre à l’utilisateur de désinstaller l’application.

Le code suivant fournit une implémentation réutilisable pour la fonctionnalité masquer l’accès, comme décrit précédemment. il peut être utilisé sur Windows XP, Windows Vista et Windows 7.


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
            // XP
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



## <a name="registering-for-application-entry-points"></a>Inscription pour les points d’entrée de l’application

Une application peut avoir de nombreux points d’entrée dans le système d’exploitation. Les emplacements recommandés pour les points d’entrée sont les suivants :

-   Bureau
-   Menu Démarrer
-   barre lancement rapide (Windows Vista et versions antérieures uniquement)
-   Zone Notifications
-   Menus contextuels
-   Bande de tâches du dossier

Cette section se concentre sur ces domaines spécifiques :

-   [Ouvrir avec](#open-with)
-   [Menu Démarrer et barre lancement rapide](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Ouvrir avec

Le menu contextuel **Ouvrir avec** permet à l’utilisateur de sélectionner une application capable de gérer un type de fichier spécifique. Bien que l’option **Ouvrir avec** puisse être utilisée pour ouvrir un fichier avec une application une fois, elle peut également être utilisée pour définir la valeur par défaut pour cette extension de nom de fichier. Par conséquent, une application doit toujours s’inscrire à **Open with** afin que les utilisateurs soient présentés avec cette application comme choix. Les applications peuvent inscrire à la fois des types de fichiers et des protocoles **ouverts avec**. Les applications qui inscrivent des protocoles dans l’infrastructure des programmes par défaut sont automatiquement ajoutées aux options **Ouvrir avec** pour les protocoles.

Pour plus d’informations sur l’inscription de pour **Open with**, consultez [Présentation des associations de fichiers](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Menu Démarrer et barre lancement rapide

Pour être plus détectable pour l’utilisateur, les applications peuvent ajouter des raccourcis vers différents emplacements dans Windows. L’emplacement le plus courant pour ajouter un raccourci est le menu **Démarrer** . dans Windows Vista et versions ultérieures, une application crée un raccourci dans le dossier caché% ProgramData% \\ Microsoft \\ Windows \\ programmes du menu démarrer \\ pour qu’ils s’affichent dans la liste des programmes du menu **démarrer** pour tous les utilisateurs. En règle générale, une application ajoute un sous-dossier qui contient le raccourci.

pour les navigateurs et les programmes de messagerie, le menu **démarrer** de Windows Vista présente également deux liens dédiés en dehors de la liste des programmes, par le biais d' **Internet** et de la **messagerie électronique**. Une fois qu’une application s’est inscrite pour ces catégories, l’infrastructure des programmes par défaut peut gérer ce qui est lancé via ces liens.

> [!Note]  
> les liens du menu **démarrer** dédié à **Internet** et au **courrier électronique** ne sont plus présents à partir de Windows 7.

 

Pour augmenter davantage la détectabilité, les applications peuvent également ajouter des raccourcis au bureau et à la barre de lancement rapide. Les applications doivent demander l’autorisation à l’utilisateur (généralement lors de l’installation ou lors de la première exécution) avant d’ajouter une icône au menu **Démarrer** , au bureau ou à la barre de lancement rapide.

> [!Note]  
> la barre lancement rapide n’est plus disponible à partir de Windows 7. l’alternative Windows 7 consiste à ce que l’application soit épinglée à la barre des tâches, mais l’épinglage ne peut pas être effectué par programmation, car il s’agit strictement d’un choix utilisateur.

 

Pour plus d’informations, consultez les rubriques suivantes :

-   [comment inscrire un navigateur Internet ou un Client de messagerie à l’aide du Menu démarrer Windows](start-menu-reg.md)
-   [Inscription de programmes avec des types de clients](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Installation et paramètres par défaut de l’application

les procédures d’installation de l’Application n’ont pas changé de façon radicale depuis Windows XP, à l’exception d’une nouvelle règle pour les systèmes exécutant des versions de Windows antérieures à Windows 8 : prendre les valeurs par défaut par ordinateur lors de l’installation, mais ne définir aucune valeur par défaut pour chaque utilisateur tant que cet utilisateur n’a pas exécuté l’application pour la première fois. (Voir la [première exécution de l’application et les valeurs par défaut](#application-first-run-and-defaults).) Les applications ne doivent pas définir les valeurs par défaut par utilisateur lors de l’installation, car il existe des situations dans lesquelles la personne qui installe l’application n’est pas l’utilisateur prévu. à partir de Windows 8, les valeurs par défaut par ordinateur ne sont pas prises en charge et les applications ne peuvent pas modifier les paramètres par défaut par utilisateur.

Pendant l’installation, une application doit copier ses fichiers binaires sur le disque dur et écrire ses ProgID dans le registre. L’application doit également s’inscrire aux programmes par défaut et **Ouvrir avec** à ce moment-là pour chaque association de fichiers qu’il est candidat à gérer. L’application peut utiliser la sous-clé **OpenWithProgIds** pour s’inscrire avec **Open with**.

Pour plus d’informations, consultez les rubriques suivantes :

-   [Programmes par défaut](default-programs.md)
-   [Présentation des associations de fichiers](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Mises à niveau et valeurs par défaut de l’application

De nombreuses applications ont la possibilité de se mettre à niveau avec le temps. Cette procédure de mise à niveau ne doit pas modifier l’état des valeurs par défaut par utilisateur, car cette modification est inattendue pour l’utilisateur. Toutefois, il est acceptable pour une application de vérifier les associations de fichiers au niveau de l’ordinateur et de les réparer si elles ont été endommagées.

## <a name="application-first-run-and-defaults"></a>Première exécution de l’application et valeurs par défaut

> [!Note]  
> à partir de Windows 8, le système gère cette procédure pour le compte de toutes les applications. Les applications elles-mêmes ne peuvent plus interroger et modifier les valeurs par défaut. Seul l’utilisateur peut le faire. Par conséquent, les applications ne doivent pas tenter d’interroger la valeur par défaut actuelle ou modifier cette valeur par défaut via un mécanisme quelconque. Toutefois, les applications peuvent fournir un point d’entrée aux programmes par défaut dans le panneau de configuration en appelant la méthode [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) de l’interface [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) .

 

avec l’introduction des paramètres par défaut par utilisateur dans Windows Vista, il est important que les applications qui contestent les extensions de nom de fichier populaires fournissent toutes une expérience utilisateur commune pour revendiquer ces extensions. Étant donné que ces valeurs par défaut sont maintenant définies dans le contexte de l’utilisateur, elles doivent se présenter comme une possibilité par défaut uniquement lorsque l’utilisateur exécute le programme après l’installation.

La règle d’établissement des valeurs par défaut par utilisateur est la suivante : lorsqu’une application est exécutée pour la première fois pour un utilisateur spécifique, cette application doit demander des préférences utilisateur pour les valeurs par défaut et les associations de fichiers pour elle-même.

L’interface utilisateur recommandée doit fournir deux choix clairs à l’utilisateur :

1.  Acceptez toutes les valeurs par défaut que l’application souhaite demander. Cette option peut également définir d’autres propriétés par défaut de l’application, telles que la confidentialité ou les paramètres de mise à jour automatique. Cette option permet à l’application de réclamer toutes ses valeurs par défaut enregistrées.
2.  Personnalisez en acceptant ou refusant les sélections par défaut et les paramètres de programme individuellement. Cette option présente une interface utilisateur supplémentaire qui permet à l’utilisateur d’effectuer des choix granulaires pour leurs options par défaut.

Pour plus d’informations, consultez [programmes par défaut](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Vérification des valeurs par défaut et demande de consentement de l’utilisateur

> [!Note]  
> Cela n’est pas pris en charge à partir de Windows 8.

 

une fois qu’une application s’est inscrite auprès des programmes par défaut dans Windows Vista et versions ultérieures, certaines api sont disponibles pour l’application. Par exemple, une application peut avoir besoin de vérifier s’il s’agit du programme par défaut. L’interface [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) fournit des méthodes pour effectuer cette opération.

Toute application qui souhaite revendiquer les valeurs par défaut doit d’abord demander à l’utilisateur et ne jamais revendiquer les valeurs par défaut sans autorisation. L’utilisateur doit être invité à indiquer s’il souhaite faire de l’application la valeur par défaut ou conserver la valeur par défaut actuelle. Il doit également y avoir une option permettant de ne pas être reposée à cette question une fois que l’utilisateur a fait son choix.

Pour plus d’informations, consultez [programmes par défaut](default-programs.md).

## <a name="application-compatibility-tips"></a>Astuces de compatibilité des applications

Cette section fournit des conseils de compatibilité des applications liés à l’expérience des programmes par défaut dans Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Éviter le déclenchement de la virtualisation Per-User

Avec l’environnement de contrôle de compte d’utilisateur (UAC), les applications doivent toujours s’exécuter avec des droits d’utilisateur standard pour une expérience client optimale. Pour des raisons de sécurité, les applications avec un niveau de privilège utilisateur standard sont bloquées lors de l’écriture dans certaines parties du Registre et dans certains fichiers système. Windows Vista et les versions ultérieures de Windows fournissent une couche de compatibilité des applications temporaire (AppCompat) pour aider les applications à effectuer la transition. Les tentatives d’écriture bloquées dans le registre ou les fichiers système sont « virtualisées » afin que l’application continue de s’exécuter, mais les zones sensibles du système ne sont pas modifiées. Toutefois, les applications ne doivent pas reposer sur la technologie AppCompat comme une solution à long terme. Au lieu de cela, les applications doivent utiliser les nombreux outils disponibles pour vérifier qu’ils peuvent s’exécuter correctement sous les droits d’utilisateur standard. Une certaine reprogrammation de l’application peut être nécessaire pour y parvenir, mais elle doit être effectuée dans l’intérêt de la compatibilité à long terme.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Éviter les avertissements ou les blocs AppCompat de l’Assistant Compatibilité des programmes

l’Assistant compatibilité des programmes (PCA) est fourni dans Windows Vista et versions ultérieures. Son objectif est de fournir une méthode automatisée pour que les anciens programmes avec des problèmes de compatibilité fonctionnent mieux. L’APC surveille les programmes à la recherche de problèmes connus. Si un problème est détecté, il avertit l’utilisateur du problème et propose d’appliquer des solutions efficaces avant que l’utilisateur n’exécute à nouveau le programme. pour éviter de voir ces avertissements ou ces blocs, les éditeurs de logiciels indépendants doivent utiliser les nombreux outils disponibles pour s’assurer que leurs applications sont compatibles avec Windows Vista, Windows 7 et versions ultérieures.

### <a name="support-for-previous-windows-operating-system-versions"></a>prise en charge des Versions précédentes du système d’exploitation Windows

l’infrastructure des programmes par défaut n’est disponible sur aucun système d’exploitation Windows avant Windows Vista. Par conséquent, lorsque les applications passent à la nouvelle infrastructure de programmes par défaut, elles doivent conserver leur code d’application par défaut plus ancien pour maintenir la compatibilité avec les versions antérieures de Windows. Une application doit exécuter une vérification de la version du système d’exploitation dans le cadre de son installation pour déterminer le code de l’application par défaut à exécuter.

pour prendre en charge une mise à niveau de Windows xp vers Windows Vista ou version ultérieure, les applications doivent ajouter toutes les entrées de registre requises pour les programmes par défaut, même lorsqu’elles sont installées sur un ordinateur exécutant Windows XP. l’inscription n’a aucun effet sur un ordinateur exécutant Windows XP, mais si l’ordinateur est mis à niveau ultérieurement, l’application est déjà inscrite et peut tirer parti de l’infrastructure.

Pour plus d’informations, consultez [**OSVersionInfo**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Ressources supplémentaires

-   [Présentation des associations de fichiers](fa-intro.md)
-   [comment inscrire un navigateur Internet ou un Client de messagerie à l’aide du Menu démarrer Windows](start-menu-reg.md)
-   [Inscription d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les associations de fichiers](fa-best-practices.md)
</dt> <dt>

[Exemple de scénario d’association de fichiers](fa-sample-scenarios.md)
</dt> <dt>

[Programmes par défaut](default-programs.md)
</dt> <dt>

[Utilisation de l’option définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
