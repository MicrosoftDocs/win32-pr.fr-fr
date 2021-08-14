---
description: Cette rubrique décrit les bibliothèques et leurs avantages pour les utilisateurs et les développeurs.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: À propos des bibliothèques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e63aef55513fb36f9a3cbfa71c1b7a79040fd7848468bd1216779cd034132d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049322"
---
# <a name="about-libraries"></a>À propos des bibliothèques

Cette rubrique décrit les bibliothèques et leurs avantages pour les utilisateurs et les développeurs.

Les bibliothèques sont des collections de dossiers définies par l’utilisateur. Une bibliothèque effectue le suivi de l’emplacement de stockage physique de chaque dossier, ce qui allège l’utilisateur et le logiciel de cette tâche. Les utilisateurs peuvent regrouper des dossiers connexes dans une bibliothèque, même si ces dossiers sont stockés sur des disques durs différents ou sur des ordinateurs différents.

Dans une bibliothèque, les dossiers et fichiers apparaissent à l’utilisateur sous la forme d’une collection unique et, à l’aide de l’API de bibliothèque de l’interpréteur de commandes, le contenu de la bibliothèque peut également sembler se trouver à un emplacement unique pour un programme.

Dans une bibliothèque, le contenu, tel que les documents, les photos, les vidéos ou la musique d’un utilisateur, peut être trié et affiché lorsque l’utilisateur le souhaite et pas simplement comme le système de fichiers le requiert. Par exemple, les utilisateurs peuvent organiser le contenu d’une bibliothèque à l’aide des propriétés des éléments de la bibliothèque afin que les éléments associés soient triés ensemble, même s’ils sont stockés dans des dossiers différents.

![capture d’écran de l’interface utilisateur des bibliothèques](images/libraries-whatare.png)

Dans cette rubrique :

-   [Avantages de la bibliothèque](#library-benefits)
    -   [Avantages de l’utilisateur](#user-benefits)
    -   [Avantages pour les développeurs](#developer-benefits)
-   [Gestion des dossiers dans les bibliothèques](#managing-folders-in-libraries)
-   [Rubriques connexes](#related-topics)

## <a name="library-benefits"></a>Avantages de la bibliothèque

Cette section décrit certains des avantages des bibliothèques du point de vue de l’utilisateur final et du point de vue du développeur de programme.

### <a name="user-benefits"></a>Avantages de l’utilisateur

L’ajout de la prise en charge de bibliothèque à votre programme offre les avantages suivants à l’utilisateur :

-   **les bibliothèques fournissent une interface utilisateur cohérente dans Windows 7**

    les boîtes de dialogue de fichier courantes prennent en charge les bibliothèques et fournissent la même expérience utilisateur que l’explorateur de Windows dans Windows 7. les bibliothèques de prise en charge dans votre programme vous aideront à fournir une interaction plus transparente pour l’utilisateur lors de l’utilisation de votre programme dans Windows 7.

-   **Les utilisateurs décident de l’emplacement de stockage du contenu**

    Les bibliothèques permettent aux utilisateurs de contrôler l’emplacement de stockage de leur contenu. En même temps, les bibliothèques fournissent des valeurs par défaut raisonnables pour les utilisateurs qui ne souhaitent pas gérer ce niveau de détail sur leur ordinateur. Les utilisateurs décident de la quantité de contrôle qu’ils veulent consacrer à l’emplacement et à la façon dont le contenu est stocké, et la bibliothèque fonctionne correctement dans les deux cas.

### <a name="developer-benefits"></a>Avantages pour les développeurs

Vous pouvez utiliser des bibliothèques dans votre programme pour fournir une interface utilisateur plus flexible et plus pratique sans avoir à ajouter beaucoup de code de programme complexe. Voici quelques-uns des avantages de l’ajout de la prise en charge de bibliothèque :

-   **Les bibliothèques prennent en charge l’accès à la bibliothèque et au système de fichiers**

    À l’aide de l’API de la [**bibliothèque Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), les programmes peuvent assurer la prise en charge de la bibliothèque pour l’utilisateur tout en réduisant la complexité du code de gestion des fichiers et des dossiers. Si votre programme utilise déjà l’API du système de fichiers, vous pouvez conserver autant de code existant que vous le souhaitez, tout en fournissant la prise en charge de la bibliothèque à l’utilisateur en obtenant les informations de système de fichiers nécessaires à partir de l’API de la bibliothèque de l' **interpréteur** de commandes.

-   **Notification de modification plus simple**

    Le système de fichiers et l’API de l’interpréteur de commandes peuvent notifier votre programme lorsque le contenu d’un dossier ou d’une bibliothèque contrôlé change. Toutefois, à l’aide de l’API Shell, vous pouvez surveiller tous les dossiers de la bibliothèque avec une seule notification, même si le dossier de la bibliothèque peut être stocké sur des lecteurs différents, voire sur des ordinateurs différents.

-   **Les bibliothèques utilisent les propriétés de fichier**

    Les programmes peuvent utiliser les propriétés de fichier pour contrôler les fichiers qui sont affichés pendant les opérations d’ouverture et d’enregistrement qui utilisent les boîtes de dialogue de fichier courantes. Les programmes peuvent également avoir accès aux propriétés de fichier à l’aide des interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Les boîtes de dialogue de fichier courantes peuvent également être configurées pour permettre aux utilisateurs de mettre à jour les propriétés associées à leur contenu.

-   **Les programmes peuvent créer des bibliothèques dédiées**

    Une nouvelle bibliothèque peut être créée lorsqu’une bibliothèque utilisateur existante ne répond pas aux besoins du programme, par exemple, si un programme crée un nouveau type de contenu utilisateur. la nouvelle bibliothèque peut être configurée avec une icône unique qui représente son contenu et facilite l’identification de la bibliothèque dans l’explorateur de Windows.

## <a name="managing-folders-in-libraries"></a>Gestion des dossiers dans les bibliothèques

Les utilisateurs peuvent organiser leurs bibliothèques en ajoutant, en déplaçant ou en supprimant des dossiers dans la bibliothèque. Toutefois, tous les dossiers ne prennent pas en charge toutes les fonctionnalités qu’une bibliothèque peut fournir. de nombreuses fonctionnalités de bibliothèque requièrent un accès rapide aux différentes propriétés du dossier et à son contenu, qui sont uniquement disponibles par le biais de Windows recherche. pour fournir une fonctionnalité de bibliothèque complète, un dossier doit pouvoir être indexé par Windows recherche.

Une bibliothèque n’autorise pas un utilisateur à ajouter des dossiers qui ne fournissent pas toutes les fonctionnalités de la bibliothèque. Toutefois, l’API de la [**bibliothèque de shells**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) peut ajouter de tels dossiers. Si une bibliothèque contient un dossier qui ne prend pas en charge la fonctionnalité de bibliothèque complète, la bibliothèque fonctionne en mode sans échec et fournit une fonctionnalité limitée. Le tableau suivant décrit les dossiers qui prennent en charge la fonctionnalité de bibliothèque complète et ceux qui ne le sont pas.



| Types de dossiers qui prennent en charge la fonctionnalité de bibliothèque complète                                                               | Types de dossiers qui ne prennent pas en charge la fonctionnalité de bibliothèque complète                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Disques durs NTFS et NTFS fixes et externes.                                                                     | Lecteurs amovibles tels que les lecteurs flash USB ou les cartes mémoire Secure Digital (SD).               |
| les partages de fichiers indexés par Windows recherche, tels que les serveurs départementaux, les Windows 7 ou les pc de bureau Windows Vista. | Support amovible, tel qu’un CD-ROM ou un DVD.                                                 |
| Les partages de fichiers qui sont disponibles hors connexion, tels qu’un dossier **Mes documents** Redirigé ou un cache Client-Side.        | Partages réseau qui ne sont pas disponibles hors connexion ni indexés à distance, tels que les lecteurs NAS.   |
|                                                                                                                    | d’autres sources de données telles que microsoft SharePoint, microsoft Exchange et Microsoft OneDrive. |



 

L’illustration suivante montre l’affichage limité du contenu de la bibliothèque en mode sans échec.

![ouvrir la boîte de dialogue lorsque les bibliothèques sont en mode sans échec](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des bibliothèques](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Liens de Shell](./links.md)
</dt> <dt>

[Dossiers connus](known-folders.md)
</dt> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> </dl>

 

 
