---
description: Le système crée un profil utilisateur la première fois qu’un utilisateur se connecte à un ordinateur. Lors des ouvertures de session suivantes, le système charge le profil de l’utilisateur, puis d’autres composants système configurent l’environnement de l’utilisateur en fonction des informations contenues dans le profil.
title: À propos des profils utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f0463a38623baa427a6ddaf3ea19b47704b90e3ef36cf91dea2469e0cd2baa00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884769"
---
# <a name="about-user-profiles"></a>À propos des profils utilisateur

Le système crée un profil utilisateur la première fois qu’un utilisateur se connecte à un ordinateur. Lors des ouvertures de session suivantes, le système charge le profil de l’utilisateur, puis d’autres composants système configurent l’environnement de l’utilisateur en fonction des informations contenues dans le profil.

## <a name="types-of-user-profiles"></a>Types de profils utilisateur

-   [Profils utilisateur locaux](local-user-profiles.md). Un profil d’utilisateur local est créé la première fois qu’un utilisateur se connecte à un ordinateur. Le profil est stocké sur le disque dur local de l’ordinateur. Les modifications apportées au profil utilisateur local sont spécifiques à l’utilisateur et à l’ordinateur sur lequel les modifications sont apportées.
-   [Profils utilisateur itinérants](roaming-user-profiles.md). Un profil utilisateur itinérant est une copie du profil local qui est copiée sur un partage de serveur et stockée sur celui-ci. Ce profil est téléchargé sur tout ordinateur auquel l’utilisateur se connecte sur un réseau. Les modifications apportées à un profil utilisateur itinérant sont synchronisées avec la copie serveur du profil lorsque l’utilisateur se déconnecte. L’avantage des profils utilisateur itinérants est que les utilisateurs n’ont pas besoin de créer un profil sur chaque ordinateur qu’ils utilisent sur un réseau.
-   Des [profils utilisateur obligatoires](mandatory-user-profiles.md). Un profil utilisateur obligatoire est un type de profil que les administrateurs peuvent utiliser pour spécifier des paramètres pour les utilisateurs. Seuls les administrateurs système peuvent apporter des modifications aux profils utilisateur obligatoires. Les modifications apportées par les utilisateurs aux paramètres du Bureau sont perdues lorsque l’utilisateur se déconnecte.
-   [Profils utilisateur temporaires](temporary-user-profiles.md). Un profil temporaire est émis chaque fois qu’une condition d’erreur empêche le chargement du profil de l’utilisateur. Les profils temporaires sont supprimés à la fin de chaque session, et les modifications apportées par l’utilisateur aux paramètres et fichiers du Bureau sont perdues lorsque l’utilisateur se déconnecte. les profils temporaires sont uniquement disponibles sur les ordinateurs qui exécutent Windows 2000 et versions ultérieures.

Un profil utilisateur se compose des éléments suivants :

-   Une ruche du Registre. La ruche du Registre est le fichier NTuser. dat. La ruche est chargée par le système lors de l’ouverture de session de l’utilisateur et est mappée à la clé de Registre **HKEY \_ Current \_ User** . La ruche du registre de l’utilisateur gère les préférences et la configuration basées sur le registre de l’utilisateur.
-   Ensemble de dossiers de profil stockés dans le système de fichiers. Les fichiers de profil utilisateur sont stockés dans le répertoire des **profils** , sur la base d’un dossier par utilisateur. Le dossier de profil utilisateur est un conteneur pour les applications et autres composants système à remplir avec des sous-dossiers, et des données par utilisateur, telles que des documents et des fichiers de configuration. Windows L’Explorateur utilise largement les dossiers de profil utilisateur pour les éléments tels que le Bureau de l’utilisateur, le menu **Démarrer** et le dossier **documents** .

Les profils utilisateur présentent les avantages suivants :

-   Lorsque l’utilisateur se connecte à un ordinateur, le système utilise les mêmes paramètres que ceux utilisés lors de la dernière fermeture de session de l’utilisateur.
-   Lors du partage d’un ordinateur avec d’autres utilisateurs, chaque utilisateur reçoit son bureau personnalisé une fois connecté.
-   Paramètres dans le profil utilisateur sont propres à chaque utilisateur. Les paramètres ne sont pas accessibles par d’autres utilisateurs. Les modifications apportées au profil d’un utilisateur n’affectent pas les autres utilisateurs ou les profils d’autres utilisateurs.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>vignettes de profil utilisateur dans Windows 7 et versions ultérieures

dans Windows 7 ou version ultérieure, une image associée est présentée à chaque profil utilisateur sous la forme d’une vignette utilisateur. Ces vignettes s’affichent pour les utilisateurs sur l’élément du panneau de configuration **comptes d’utilisateur** et sa sous-page **gérer les comptes** . Les fichiers image de l’invité par défaut et les comptes d’utilisateur par défaut s’affichent également ici si vous disposez des droits d’accès administrateur.

> [!Note]  
> La sous-page **gérer les comptes** est accessible via le lien **gérer un autre compte** de l’élément du panneau de configuration **comptes d’utilisateur** .

 

-   % ProgramData% \\ d' \\ images de compte d’utilisateur Microsoft \\Guest.bmp
-   % ProgramData% \\ d' \\ images de compte d’utilisateur Microsoft \\User.bmp

L’image de vignette de l’utilisateur est stockée dans le \\ dossier Temp local% Systemdrive% Users \\ <username> \\ AppData \\ \\ comme <username>.bmp. Les caractères de barre oblique ( \\ ) sont convertis en caractères de signe plus (+). Par exemple, l' \\ utilisateur de domaine est converti en domaine + utilisateur.

Le fichier image s’affiche dans le dossier **temp** de l’utilisateur :

-   Une fois que l’utilisateur a terminé la configuration initiale du système (OOBE).
-   Lorsque l’utilisateur lance pour la première fois l’élément du panneau de configuration **comptes d’utilisateur** .
-   Lorsque l’utilisateur accède à la sous-page **gérer les comptes** de l’élément du panneau de configuration **comptes d’utilisateur** . En outre, les vignettes de tous les autres utilisateurs sur l’ordinateur sont affichées.

Ces instances sont le seul moment où les images sont créées ou mises à jour. Par conséquent, il y a plusieurs points à prendre en compte lors de l’utilisation de l’emplacement du dossier **temporaire** par programme :

1.  Il n’est pas garanti que la vignette de l’utilisateur soit présente. Si l’utilisateur supprime le fichier .bmp, par exemple manuellement ou à l’aide d’un utilitaire qui supprime les fichiers temporaires, cette vignette utilisateur n’est pas recréée automatiquement tant que l’utilisateur n’a pas lancé la sous-page gérer les **comptes d’utilisateurs** ou **gérer les comptes** .

2.  Les vignettes de l’utilisateur pour d’autres utilisateurs sur l’ordinateur ne sont peut-être pas présentes dans le dossier **temporaire** de l’utilisateur actuellement connecté. par exemple, si l’utilisateur A crée l’utilisateur b par le biais de l’élément du panneau de configuration **comptes d’utilisateur** , la vignette de l’utilisateur b est créée dans le dossier **temporaire** de l’utilisateur a lorsque Windows envoie l’utilisateur a à la sous-page **gérer les comptes** . Étant donné que la structure de répertoires n’est pas créée pour l’utilisateur B tant qu’il n’est pas connecté, le dossier **temporaire** de l’utilisateur a est le seul emplacement où la vignette de l’utilisateur b est stockée. Lorsque l’utilisateur B ouvre une session, la seule image stockée dans le dossier **temp** de l’utilisateur b est sa propre.

    1.  Pour obtenir toutes les vignettes de l’utilisateur pour les utilisateurs d’un système, les applications devront peut-être effectuer une recherche dans le répertoire **temp** de chaque utilisateur.
    2.  Étant donné que la liste de contrôle d’accès (ACL) de ces répertoires **temporaires** autorise l’accès au système, à l’administrateur et à l’utilisateur actuel, les applications doivent s’élever à l’accès pour d’autres utilisateurs.

3.  Il n’est pas garanti que les vignettes d’autres utilisateurs soient à jour dans leurs dossiers **temporaires** . Si l’utilisateur B met à jour sa vignette d’utilisateur, l’utilisateur A ne voit pas la modification tant que l’utilisateur A n’A pas accès à la sous-page **gérer les comptes** . Par conséquent, si les applications utilisent le dossier **temporaire** de l’utilisateur A pour obtenir la vignette de l’utilisateur B, ces applications peuvent obtenir un fichier image obsolète.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Profils utilisateur locaux](local-user-profiles.md)
</dt> <dt>

[Profils utilisateur itinérants](roaming-user-profiles.md)
</dt> <dt>

[Profils utilisateur obligatoires](mandatory-user-profiles.md)
</dt> <dt>

[Profils utilisateur temporaires](temporary-user-profiles.md)
</dt> <dt>

[Répertoire des profils](profiles-directory.md)
</dt> <dt>

[Variables d’environnement utilisateur](user-environment-variables.md)
</dt> <dt>

[Changement rapide d'utilisateur](fast-user-switching.md)
</dt> </dl>

 

 



