---
description: donne une vue d’ensemble des modifications apportées à la Windows les contrôles parentaux introduits dans Windows 8.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: nouveautés de Windows 8 la sécurité des familles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e67714618f691a61490900c8d7d35bf3cc462d8f7c86cdeccb9120aa3c519554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951679"
---
# <a name="whats-new-in-windows-8-family-safety"></a>nouveautés de Windows 8 la sécurité des familles

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Vue d’ensemble des modifications de contrôle parental pour Windows 8

l’objectif de ce document est de fournir une vue d’ensemble des modifications apportées au contrôle parental Windows dans Windows 8 et d’autoriser les fournisseurs de solutions de contrôle parental tiers à tirer parti de ces modifications. ce document suppose que les lecteurs sont familiers avec les contrôles de contrôle parental pour Windows 7 et Windows Vista et qu’ils reflètent uniquement les modifications apportées à cette fonctionnalité dans Windows 8 qui sont pertinentes pour le développement de solutions de contrôle Parental tierces.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>décisions de conception clés pour Windows 8 modifications du contrôle Parental/sécurité des familles

les modifications apportées aux contrôles de contrôle parental introduites dans Windows 8 poursuivent l’objectif principal de l’introduction des améliorations de fonctionnalités et de la promotion de la coexistence de solutions de contrôle parental tierces avec la fonctionnalité intégrée. Les modifications sont les suivantes :

-   utilisation de Microsoft Family Safety pour assurer la gestion à distance et l’analyse de l’activité à distance.
-   intégration du filtrage web dans le cadre des restrictions Microsoft et de la capacité à afficher les rapports d’activité sur un ordinateur Windows 8.
-   La fonctionnalité de contrôle parental du panneau de configuration a été renommée sécurité des familles et sera désignée comme telle dans ce document.
-   Les restrictions de temps intégrées ont été améliorées grâce à la possibilité de contrôler la durée totale d’utilisation de l’ordinateur par jour (durée), en plus de la possibilité de contrôler les heures d’utilisation de l’ordinateur (curfew). Curfew était disponible dans les versions précédentes de Windows.
-   Windows 8 Les fonctionnalités de sécurité des familles peuvent être activées pendant le processus de création de compte standard.
-   Windows les fonctionnalités d’extensibilité des contrôles parentaux Vista et Windows 7 continuent d’être prises en charge par la sécurité de la famille de Windows 8, y compris par les solutions tierces pour remplacer le filtre de contenu web ou pour remplacer l’interface utilisateur de configuration intégrée tout en continuant à utiliser la mise en œuvre intégrée du temps, de l’Application, des Restrictions de jeu et du filtre de contenu web.
-   l’activation d’un fournisseur tiers désactive la gestion à distance et la création de rapports d’Windows 8 contrôles de sécurité des familles via un site web de sécurité de famille.
-   l’extensibilité tierce pour la sécurité des familles est prise en charge uniquement pour les applications de bureau Windows 8.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>La sécurité des familles et la création de comptes standard dans Windows 8

dans le cadre de la création de comptes standard dans Windows 8, un administrateur a la possibilité d’activer la surveillance du compte par la sécurité des familles. La liste suivante répertorie les fonctionnalités et la capacité du fournisseur tiers à les contrôler :

-   dans le dernier écran de Windows 8 le processus de création de compte standard, un administrateur reçoit une case à cocher pour activer la sécurité des familles pour le compte nouvellement créé.
-   Si cette case est cochée, le contrôle parental est activé pour le compte avec les paramètres suivants :
    -   Rapports d’activité sur
    -   Toutes les restrictions sont désactivées
-   si l’administrateur a utilisé un compte Microsoft pour se connecter à Windows, le Windows 8 ordinateur est configuré pour la gestion à distance des paramètres de sécurité des familles et des rapports d’activité de messagerie. Le site Web de sécurité de famille peut ensuite être utilisé pour gérer un tel ordinateur à distance.
-   Si le fournisseur tiers souhaite que la case à cocher soit présente dans un workflow de création de compte standard, la valeur suivante doit être présente parmi les valeurs d’inscription du fournisseur. pour plus d’informations sur les détails de l’inscription du fournisseur, consultez la section [inscription du fournisseur](what-s-new-in-windows-7-parental-controls.md) dans la rubrique nouveautés de Windows 7 contrôle Parental.

    

    | Terme                                                                                                                         | Description                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | valeur différente de zéro **DWORD** facultative qui spécifie que l’option de case à cocher permettant d’activer la surveillance de la sécurité de famille pour un compte nouvellement créé doit être visible lors de la création du compte standard dans Windows 8 une fois que le fournisseur est sélectionné en tant que fournisseur de sécurité de famille actuel.<br/> |

    

     

-   Étant donné que les fournisseurs tiers sont conçus pour remplacer l’interface utilisateur de configuration intégrée pour les contrôles de sécurité des familles, par défaut, l’installation et l’activation d’un fournisseur tiers entraînent l’activation de la case à cocher pour activer la sécurité de la famille pendant la création du compte standard.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Modifications de l’interface utilisateur de niveau supérieur pour la sécurité de famille dans Windows 8

Windows 8 apporte les modifications suivantes à l’interface utilisateur de niveau supérieur du panneau de configuration du contrôle Parental :

-   quand les contrôles de sécurité de la famille sont activés pour au moins un compte standard sur un ordinateur Windows 8, le lien gérer les paramètres sur le site web de sécurité de famille s’affiche et permet à un administrateur d’établir une gestion à distance des paramètres de sécurité de la famille de Windows 8 ordinateur via le site web de sécurité de famille.
-   lorsqu’un ordinateur Windows 8 est configuré pour la gestion à distance via un site web de sécurité de famille, le contrôle plus d’informations permet à un administrateur de désactiver la gestion à distance d’un Windows 8 ordinateur via le site web de sécurité de famille.
-   La section contrôles est visible uniquement lorsqu’au moins un fournisseur tiers est inscrit avec la sécurité parentale. l’interface utilisateur et les fonctionnalités de cette section sont identiques à celles de la section contrôles supplémentaires dans Windows 7 contrôle Parental. pour plus d’informations, consultez la section contrôle parental modifications de l’interface utilisateur de niveau supérieur de la rubrique [Windows 7 contrôle parental](what-s-new-in-windows-7-parental-controls.md) .
-   lorsqu’un fournisseur tiers est installé et sélectionné en tant que fournisseur actuel, la gestion à distance de Windows 8 paramètres de sécurité de la famille d’ordinateurs via le site web de sécurité de famille est désactivée.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Modifications des restrictions de In-Box de sécurité des familles dans Windows 8

Windows 8 apporte les modifications suivantes aux restrictions de sécurité de la famille :

Restrictions Web

-   l’implémentation est passée d’un filtre LSP (layered Service Provider) à un pilote de plateforme de filtrage Windows (WFP) communiquant avec le processus de surveillance de la sécurité des familles en cours d’exécution dans les sessions des utilisateurs.

Limites de temps

-   Les restrictions de temps intégrées ont été améliorées grâce à la possibilité de contrôler la durée totale d’utilisation de l’ordinateur par jour (durée), en plus de la possibilité de contrôler les heures d’utilisation de l’ordinateur (curfew) disponibles dans les versions précédentes de Windows.
-   L’interface utilisateur pour curfew permet un contrôle indépendant pour chaque jour de la semaine avec une granularité de demi-heure.
-   L’interface utilisateur pour l’allocation de temps autorise des contrôles pour les jours de semaine/week-ends ou le contrôle indépendant pour chaque jour de la semaine avec une granularité de 15 minutes.
-   Le mécanisme de changement rapide d’utilisateur n’est plus utilisé pour forcer le verrouillage ou bloquer la connexion de l’utilisateur contrôlé en cas de délai de blocage. Un basculement vers un bureau distinct est utilisé à ces fins.
-   Les événements d’avertissement de déconnexion ne sont plus disponibles pour s’abonner à des applications.

## <a name="family-safety-api-changes-in-windows-8"></a>Modifications de l’API de sécurité des familles dans Windows 8

Les API utilisées pour la sécurité des familles exposent les paramètres des restrictions de stratégie et d’archivage, ainsi que la fonctionnalité de journalisation.

Journalisation

-   Les événements personnalisés ne sont plus pris en charge dans la visionneuse de rapports d’activité de sécurité de famille.

API WMI Paramètres écriture/lecture

-   WpcUserSettings-auparavant, les restrictions de minuterie prenait en charge une granularité de 1 heure. dans Windows 8 la propriété existante représente la première demi-heure pour chaque heure. Une nouvelle propriété de demi-heure a été ajoutée pour représenter la seconde moitié de chaque heure. Une nouvelle propriété supplémentaire a été introduite pour représenter le délai quotidien.

Filtre de contenu Web autoriser/bloquer l’exportation/importation d’un format

-   La fonctionnalité d’exportation du filtre de contenu Web n’est plus prise en charge.

schéma du fournisseur WMI de famille Paramètres

-   Les ajouts suivants ont été apportés à la classe WpcUserSettings pour refléter les améliorations des restrictions de temps :
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 utilise une nouvelle clé de registre pour indiquer que l’API de sécurité de famille est activée pour un utilisateur donné.
>
> **HKLM** \\ **Microsoft** \\ **Logiciel** \\ **Windows** \\ **CurrentVersion** \\ **Contrôle parental** \\ **Utilisateurs** \\ **{UserSid}** \\ **Web** \\ **Filtrer sur**

 

la clé de registre suivante est prise en charge pour Windows 7 uniquement.

**HKLM** \\ **Microsoft** \\ **Logiciel** \\ **Windows** \\ **CurrentVersion** \\ **Contrôle parental** \\ **Utilisateurs** \\ **{UserSid}** \\ **Contrôle parental activé**

Pour les deux clés, la valeur « 0x00 » (**DWORD**) indique que la fonctionnalité est désactivée pour l’utilisateur actuel et la valeur « 0x01 » (**DWORD**) indique que la fonctionnalité est activée pour l’utilisateur actuel. Lorsque vous tentez de lire les valeurs de ces clés, remplacez le jeton « {UserSid} » par l’ID système de l’utilisateur.

 

 




