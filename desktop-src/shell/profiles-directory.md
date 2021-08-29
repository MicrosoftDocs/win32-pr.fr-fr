---
description: 'le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans les différentes versions de Windows : &\# 0034 ; Documents et Paramètres&\# 0034 ; dans Windows XP et &\# 0034 ; les utilisateurs&\# 0034 ; dans Windows Vista et versions ultérieures.'
title: Répertoire des profils
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40e9f795c800a3a688f3b032db53cba755849db6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467246"
---
# <a name="profiles-directory"></a>Répertoire des profils

le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans les différentes versions de Windows : « Documents et Paramètres » dans Windows XP et « utilisateurs » dans Windows Vista et versions ultérieures. Pour obtenir le chemin d’accès du répertoire des profils, utilisez la fonction [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .

Le répertoire des profils contient les sous-répertoires suivants pour les profils utilisateur.



| Répertoire                                      | Description                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista ou version ultérieure)/all users | Informations de programme qui s’appliquent à tous les utilisateurs. le répertoire tous les utilisateurs existe toujours dans Windows Vista ou version ultérieure, pour des raisons de compatibilité descendante. |
| Par défaut                                        | Informations de profil qui s’appliquent à l’utilisateur par défaut.                                                                                      |
| *Utilisateur*                                         | Informations de profil qui s’appliquent à l’utilisateur spécifié. Chaque utilisateur possède son propre sous-répertoire de profil.                                      |



 

Pour obtenir l’emplacement du répertoire ProgramData/All Users, appelez la fonction [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) . Le répertoire contient les sous-répertoires suivants :



| Répertoire  | Description                          |
|------------|--------------------------------------|
| Bureau    | Raccourcis à afficher sur le bureau. |
| Menu Démarrer | Éléments de menu du menu **Démarrer** .   |



 

Pour obtenir l’emplacement de l’annuaire de l’utilisateur par défaut, appelez la fonction [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) . Pour obtenir l’emplacement de l’annuaire d’un utilisateur particulier, appelez la fonction [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) . Les répertoires utilisateur par défaut et utilisateurs spécifiques contiennent les sous-répertoires suivants. Les répertoires en italique indiquent les répertoires qui sont masqués par défaut. Vous pouvez afficher ces répertoires en sélectionnant l’option **afficher les fichiers, les dossiers et les lecteurs masqués** dans les **Options des dossiers** , élément du panneau de configuration.




| Répertoire | Description | 
|-----------|-------------|
| Données d'application | Données spécifiques à l’application. | 
| Cookies | Windows Cookies Internet Explorer. | 
| Bureau | Raccourcis à afficher sur le bureau. | 
| Favoris | Liens vers les sites Web favoris. | 
| Paramètres Local | Paramètres et données d’application qui ne sont pas itinérants avec le profil. En général, les paramètres ou les données de ce répertoire sont spécifiques à l’ordinateur ou ils sont trop volumineux pour être itinérants efficacement. Ce répertoire contient les sous-dossiers suivants :<ul><li>Données d'application</li><li>Historique</li><li>Temp</li><li>Fichiers Internet temporaires</li></ul> | 
| Mes documents | Emplacement par défaut des documents créés par l’utilisateur. Les applications doivent enregistrer les fichiers de documents dans ce répertoire par défaut. | 
| <em>Nethotte</em> | Raccourcis vers les éléments du voisinage réseau. | 
| <em>PrintHood</em> | Raccourcis vers des éléments de dossier d’imprimante. | 
| <em>Sources</em> | Raccourcis vers les documents les plus récemment utilisés. | 
| SendTo | Raccourcis vers les emplacements auxquels l’utilisateur envoie souvent des fichiers. | 
| Menu Démarrer | Éléments de menu du menu <strong>Démarrer</strong> . | 
| <em>Modèles</em> | Raccourcis vers les éléments de modèle. | 




 

Pour obtenir l’emplacement des sous-répertoires de ces répertoires, utilisez les fonctions [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ou [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

 

 



