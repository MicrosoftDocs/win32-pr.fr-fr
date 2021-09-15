---
description: Cette rubrique décrit les fonctionnalités définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD) disponibles dans le panneau de configuration.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412567"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)

Cette rubrique décrit les fonctionnalités **définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)** disponibles dans le panneau de configuration. la commande SPAD se trouve sous l’élément [programmes par défaut](default-programs.md) du panneau de configuration dans Windows Vista et les versions ultérieures de Windows. dans Windows XP, il se trouve dans l’élément **ajouter ou supprimer des programmes** et intitulé **définir l’accès aux programmes et les valeurs par défaut**.

> [!IMPORTANT]
> Cette rubrique ne s’applique pas à Windows 10. La façon dont les associations de fichiers par défaut fonctionnent dans Windows 10. pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Utilisation de l’outil définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Vue d’ensemble de la configuration des paramètres par défaut de l’accès aux programmes et de l’ordinateur](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Valeur de Registre LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtrage de la liste Ajout/suppression de programmes](#filtering-the-add-or-remove-programs-list)
-   [Ressources supplémentaires](#filtering-the-add-or-remove-programs-list)
-   [Rubriques connexes](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Utilisation de l’outil définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur

> [!Note]  
> à partir de Windows 8, SPAD configure les valeurs par défaut pour chaque utilisateur pour l’utilisateur actuel. avant Windows 8, SPAD définissant les valeurs par défaut par ordinateur. Lorsqu’une valeur par défaut par utilisateur n’a pas encore été configurée par l’utilisateur, le système lui demande de définir une valeur par défaut par l’utilisateur plutôt que de revenir sur une valeur par défaut par ordinateur. il est possible que les valeurs par défaut par ordinateur n’aient jamais été vues par les utilisateurs dans Windows Vista et Windows 7 s’ils avaient déjà défini des valeurs par défaut par utilisateur, car les valeurs par défaut par utilisateur remplacent les valeurs par défaut par ordinateur dans ces systèmes d’exploitation.

 

dans Windows XP, l’option **définir l’accès aux programmes et les valeurs par défaut** est un outil qui se trouve sous la forme d’une option dans l’élément **ajout/suppression de programmes** du panneau de configuration. dans Windows Vista et versions ultérieures, il se trouve sous l’élément [programmes par défaut](default-programs.md) du panneau de configuration. Pour les programmes [inscrits](reg-middleware-apps.md) , il exécute les fonctions suivantes :

-   active le choix des programmes par défaut pour chaque type de client (jusqu’à Windows 7 uniquement).
-   Permet de contrôler l’affichage des icônes, raccourcis et entrées de menu du programme.
-   Fournit un ensemble de choix de programmes par défaut prédéfinis. (Windows XP Service Pack 1 (SP1) uniquement)

Cet outil est utilisé pour les cinq types de clients suivants.

-   Browser
-   E-mail
-   Programme messenging instantanée
-   Lecteur multimédia
-   Machine virtuelle pour Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Vue d’ensemble de la configuration des paramètres par défaut de l’accès aux programmes et de l’ordinateur

la page **définir les paramètres par défaut pour l’accès aux programmes et** les Windows 8 s’affiche dans la capture d’écran suivante.

![capture d’écran de l’affichage définir l’accès aux programmes et les paramètres par défaut de l’ordinateur](images/spad-initial.png)

Trois options de configuration possibles sont présentées à l’utilisateur, avec la possibilité pour les fabricants OEM de présenter une quatrième option intitulée « fabricant de l’ordinateur ».

-   [Microsoft Windows](#microsoft-windows)
-   [Non-Microsoft](#non-microsoft)
-   [Personnalisée](#custom)
-   [Fabricant de l'ordinateur](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

la configuration **Microsoft Windows** se compose d’un ensemble de programmes par défaut fournis avec Windows, comme illustré dans la capture d’écran suivante.

![capture d’écran de l’option définir l’accès aux programmes et les valeurs par défaut Microsoft](images/mspage.png)

la sélection de la configuration **Microsoft Windows** permet également d’afficher les icônes, les raccourcis ou les entrées de menu pour chaque programme enregistré pour l’un des cinq types de client. Ces icônes, raccourcis et entrées de menu sont disponibles pour l’utilisateur dans le menu **Démarrer** ou l’écran d’accueil, sur le bureau et dans tous les autres emplacements auxquels ils ont été ajoutés.

### <a name="non-microsoft"></a>Non-Microsoft

La configuration **non-Microsoft** , présentée dans la capture d’écran suivante, est utilisée pour les applications inscrites sur le système de l’utilisateur qui ne sont pas générées par Microsoft. Ces applications peuvent être préinstallées sur le système de l’utilisateur, ou il peut s’agir d’applications non Microsoft que l’utilisateur a installées.

> [!Note]  
> Les applications doivent s’inscrire pour apparaître sur cette page. Pour obtenir des instructions sur l’inscription d’une application, consultez [inscription de programmes avec des types de clients](reg-middleware-apps.md).

 

![capture d’écran des options Set Program Access et non-Microsoft par défaut](images/nonmspage.png)

la sélection de l’option **non-Microsoft** supprime également l’accès aux icônes, raccourcis et entrées de menu des programmes microsoft listés dans la configuration [microsoft Windows](#microsoft-windows) pour tous les types de clients qui en ont. Ces icônes, raccourcis et entrées de menu Microsoft sont supprimés du menu **Démarrer** , du bureau et d’autres emplacements auxquels ils ont été ajoutés.

### <a name="custom"></a>Custom

La configuration **personnalisée** , présentée dans la capture d’écran suivante, permet aux utilisateurs de personnaliser leurs systèmes avec n’importe quelle combinaison de programmes Microsoft et non-Microsoft enregistrés comme possibilités par défaut pour les cinq types de clients. il s’agit de la seule parmi les quatre options disponibles dans Windows 2000 Service Pack 3 (SP3).

![capture d’écran des options personnalisées d’accès aux programmes et par défaut](images/custompage.png)

toutes les options présentées dans les configurations [microsoft Windows](#microsoft-windows) et [Non-microsoft](#non-microsoft) sont disponibles pour l’utilisateur dans la section **personnalisée** , ainsi que pour toutes les applications microsoft installées qui ne font pas partie de Windows. La case d’option **utiliser mon navigateur Web actuel** est présélectionnée, comme illustré dans la capture d’écran précédente. Il n’existe aucun moyen de déterminer le navigateur par défaut actuel à partir de l’interface utilisateur. l’appel de liens web ou de fichiers dans Windows est la seule façon de découvrir le navigateur par défaut actuel.

lorsqu’un utilisateur active la case à cocher **activer l’accès à ce programme** pour un programme, les icônes, les raccourcis et les entrées de menu de ce programme s’affichent dans la menu Démarrer ou l’écran de démarrage, sur le bureau ou dans tout autre emplacement où ils ont été installés. Si vous désactivez cette option, vous devez supprimer ces icônes, raccourcis et entrées de menu, mais le comportement de ces options dépend entièrement du fournisseur de l’application. Windows ne contrôle pas la façon dont l’accès est activé ou supprimé dans toute l’interface utilisateur. Il est également important de comprendre que les applications ne sont pas obligées de s’inscrire pour **définir les paramètres par défaut de l’accès aux programmes et de l’ordinateur**.

### <a name="computer-manufacturer"></a>Fabricant de l'ordinateur

Une quatrième catégorie intitulée « fabricant de l’ordinateur » peut apparaître dans la fenêtre SPAD sur certains systèmes. Les fabricants d’ordinateurs peuvent choisir de préconfigurer leurs ordinateurs avec un ensemble personnalisé de valeurs par défaut, en choisissant parmi les mêmes sélections disponibles dans la configuration [personnalisée](#custom) . (À des fins d’illustration, un ensemble fictif d’applications nommé LitWare est inscrit pour être utilisé avec tous les types de clients.) un utilisateur peut revenir à la configuration par défaut du fabricant de l’ordinateur à tout moment en choisissant l’option fabricant de l' **ordinateur** , comme indiqué dans la capture d’écran suivante Windows XP.

> [!Note]  
> Cette configuration n’apparaît pas sur tous les systèmes. Pour plus d’informations, reportez-vous au kit de préinstallation OEM (OPK).

 

![capture d’écran des options Set Program Access et default Computer Manufacturer](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Valeur de Registre LastUserInitiatedDefaultChange

La valeur LastUserInitiatedDefaultChange a été ajoutée au registre pour aider les applications à reconnaître et respecter les choix par défaut de l’utilisateur. La valeur contient \_ des données binaires reg sous la forme d’une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui contient la date et l’heure (au format UTC) de la dernière modification par l’utilisateur d’un choix par défaut par le biais de l’outil **définir l’accès aux programmes et les paramètres par défaut** de l’ordinateur. Cette valeur se trouve sous la sous-clé suivante.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

Le scénario suivant utilise cette valeur pour une application qui surveille les associations de fichiers.

1.  Une application enregistre en interne l’heure à laquelle elle a été définie en tant que programme par défaut pour son type de client (au moment de l’installation ou ultérieurement).
2.  L’application détecte que le programme par défaut pour son type de client a été remplacé par un programme autre que lui-même ou par l’application qu’elle représente (dans le cas des programmes d’assistance en arrière-plan). Non pris en charge dans Windows 8.
3.  L’application lit la valeur de LastUserInitiatedDefaultChange (l’horodatage de la dernière modification par défaut initiée par l’utilisateur) et la compare à la valeur d’horodatage stockée pour son propre choix par défaut.
4.  Si LastUserInitiatedDefaultChange est postérieure à la valeur stockée de l’application, aucune action ne doit être prise par cette application, car la modification a été explicitement demandée par l’utilisateur via l’outil **définir l’accès aux programmes et les paramètres par défaut** .
5.  L’application ne surveille plus cette association de fichiers jusqu’à ce qu’elle soit à nouveau choisie comme valeur par défaut. Non pris en charge dans Windows 8.

En adhérant à un tel schéma, les souhaits de l’utilisateur sont respectés et leur propriétaire ultime de leurs systèmes est conservé.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtrage de la liste Ajout/suppression de programmes

> [!Note]  
> cette section s’applique à Windows XP Service Pack 2 (SP2) et versions ultérieures, ainsi qu’à Windows Server 2003 et versions ultérieures.

 

dans Windows XP et Windows Server 2003, la liste des applications affichées sous l’onglet **modifier ou supprimer des programmes** sous **ajout/suppression de programmes** peut être filtrée par l’utilisateur pour exclure les entrées pour les mises à jour d’application. dans ces versions de Windows, cela s’effectue à l’aide d’une case à cocher **afficher les mises à jour** en haut de la fenêtre. L’option **afficher les mises à jour** n’est pas sélectionnée par défaut. par conséquent, les mises à jour ne sont *pas* affichées, sauf si l’utilisateur choisit de les afficher. Les modifications apportées à l’état de la case à cocher persistent lorsque **Ajout/suppression de programmes** est fermé. Si un utilisateur choisit d’afficher les mises à jour, celles-ci continuent d’être affichées jusqu’à ce que l’utilisateur désactive la case à cocher.

> [!Note]  
> la mise à jour Windows XP SP2 elle-même est une exception au filtrage. Elle est toujours affichée indépendamment de l’état de la case à cocher.

 

dans Windows Vista et versions ultérieures, les mises à jour d’application sont affichées sur une page distincte dans le panneau de configuration dédié aux mises à jour uniquement. Cette page s’affiche lorsque l’utilisateur clique sur le lien Afficher la tâche des **mises à jour installées** . Il n’existe aucune option sélectionnable par l’utilisateur pour afficher les mises à jour sur la même page que les programmes installés. Malgré la modification de l’interface utilisateur, le mécanisme d’inscription en tant que mise à jour d’un programme installé reste le même que dans les versions antérieures de Windows.

les applications microsoft et non-microsoft qui utilisent la Windows Installer n’ont rien à faire pour que leurs mises à jour soient reconnues comme des mises à jour. les applications non-Microsoft qui n’utilisent pas Windows Installer doivent déclarer certaines valeurs dans le registre dans le cadre de leur installation pour être reconnues comme une mise à jour d’un programme existant.

L’exemple suivant illustre les valeurs de Registre à déclarer pour qu’une installation soit reconnue comme une mise à jour d’un programme existant.

1.  l’application parente doit ajouter ses informations de désinstallation dans une sous-clé sous la sous-clé **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **uninstall** . Pour plus d’informations sur l’utilisation de la sous-clé **Uninstall** , consultez la rubrique [installation](/previous-versions/ms997548(v=msdn.10)) .
2.  Chaque mise à jour de cette application parente doit également ajouter ses informations sous la forme d’une sous-clé de la sous-clé **Uninstall** . Il doit utiliser une convention d’affectation de noms particulière de son choix, en tentant d’éviter les conflits potentiels avec d’autres programmes. les conventions suivantes sont réservées en tant que noms de sous-clés par Microsoft pour une utilisation avec des mises à jour Windows.
    -   IEUpdate
    -   OEUpdate
    -   « KB » suivi de six chiffres, par exemple « KB123456 »
    -   « Q » suivi de six chiffres, par exemple « Q123456 »
    -   Six chiffres, par exemple « 123456 »
3.  En plus des informations de désinstallation standard ajoutées pour l’application parente, les sous-clés de chaque mise à jour doivent inclure deux des trois entrées suivantes. Leurs valeurs sont de type REG \_ sz.
    -   **ParentKeyName**. Cette valeur est requise. Il s’agit du nom de la sous-clé du parent déclarée à l’étape 1. Cela associe la mise à jour au programme.
    -   **ParentDisplayName**. Cette valeur est requise. Si aucune sous-clé ne correspond à celle nommée dans ParentKeyName, cette valeur est utilisée comme un programme parent d’espace réservé à afficher dans **Ajout/suppression de programmes**.
    -   **InstallDate**. Cette valeur est facultative. Il doit utiliser le formulaire `yyyymmdd` pour spécifier la date. Cette date est utilisée pour le **installé sur** les informations affichées en regard de l’entrée de la mise à jour dans l’interface utilisateur. S’il n’existe aucune entrée **InstallDate** ou si elle est présente mais n’a pas de valeur assignée, voici ce qui se produit :
        -   versions de système d’exploitation autres que Windows Vista et Windows 7 : aucun **installé sur** les informations n’est affiché.
        -   Windows Vista et versions ultérieures : une date par défaut est utilisée. Il s’agit de la date de « dernière modification » de l’une des entrées de la sous-clé de cette mise à jour. Il s’agit normalement du jour où la mise à jour a été ajoutée au registre. Toutefois, étant donné qu’il s’agit d’une date de « dernière modification », toute modification ultérieure apportée à l’une des entrées de la sous-clé entraîne la modification de la valeur InstallDate à la date de cette modification.

L’exemple suivant montre les entrées de Registre pertinentes pour une mise à jour de l’application LitWare Deluxe.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

Les applications non-Microsoft qui ne fournissent pas les informations de Registre appropriées, telles que les mises à jour produites avant la disponibilité de cette option, continuent de s’afficher normalement dans la liste des programmes installés et ne sont pas filtrées.

le filtrage des mises à jour dans les versions de système d’exploitation autres que Windows Vista et Windows 7 est normalement un paramètre contrôlé par l’utilisateur et doit être respecté en tant que tel par les applications. Toutefois, dans un environnement d’entreprise, les administrateurs peuvent contrôler si les utilisateurs ont la possibilité de filtrer les mises à jour via la valeur de Registre DontGroupPatches, comme illustré dans l’exemple suivant.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

Cette valeur est de type REG \_ DWORD et est interprétée comme suit.



| Valeur DontGroupPatches             | Signification                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | La case à cocher **afficher les mises à jour** s’affiche pour l’utilisateur. Le filtrage varie selon que l’utilisateur a activé ou non cette case à cocher.                                                                                         |
| 1                                  | La case à cocher **afficher les mises à jour** est supprimée de l’interface utilisateur. Les mises à jour ne sont pas filtrées à partir de la liste. cette valeur revient principalement au comportement Windows XP SP1, avant l’introduction de la fonctionnalité **afficher les mises à jour** . |
| Entrée DontGroupPatches absente | Cela équivaut à définir la valeur sur 0.                                                                                                                                                                       |



 

DontGroupPatches n’a aucun effet dans Windows Vista et Windows 7, où l’interface utilisateur ne contient pas de case à cocher et les mises à jour inscrites sont toujours filtrées.

> [!Note]  
> Les stratégies sont définies uniquement par les administrateurs. Les applications ne doivent pas modifier cette valeur. pour plus d’informations sur la définition d’une stratégie de groupe basée sur le registre, consultez [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page) ou [Windows Server stratégie de groupe](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Ressources supplémentaires

-   [Inscription de programmes avec des types de clients](reg-middleware-apps.md)
-   [Installation](/previous-versions/ms997548(v=msdn.10))
-   [configuration de l’ajout/suppression de programmes avec Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les associations de fichiers](fa-best-practices.md)
</dt> <dt>

[Exemple de scénario d’association de fichiers](fa-sample-scenarios.md)
</dt> <dt>

[instructions pour la gestion des Applications par défaut dans Windows Vista et versions ultérieures](vista-managing-defaults.md)
</dt> <dt>

[Programmes par défaut](default-programs.md)
</dt> </dl>

 

 
