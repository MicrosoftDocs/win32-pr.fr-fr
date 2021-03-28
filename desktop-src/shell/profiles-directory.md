---
description: 'Le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans différentes versions de Windows : &\# 0034 ; documents and settings&\# 0034 ; dans Windows XP et &\# 0034 ; Les utilisateurs&\# 0034 ; dans Windows Vista et versions ultérieures.'
title: Répertoire des profils
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973347"
---
# <a name="profiles-directory"></a>Répertoire des profils

Le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans les différentes versions de Windows : « documents and Settings » sous Windows XP et « Users » dans Windows Vista et versions ultérieures. Pour obtenir le chemin d’accès du répertoire des profils, utilisez la fonction [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .

Le répertoire des profils contient les sous-répertoires suivants pour les profils utilisateur.



| Répertoire                                      | Description                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista ou version ultérieure)/All Users | Informations de programme qui s’appliquent à tous les utilisateurs. Le répertoire tous les utilisateurs existe toujours dans Windows Vista ou version ultérieure, pour des raisons de compatibilité descendante. |
| Default                                        | Informations de profil qui s’appliquent à l’utilisateur par défaut.                                                                                      |
| *Utilisateur*                                         | Informations de profil qui s’appliquent à l’utilisateur spécifié. Chaque utilisateur possède son propre sous-répertoire de profil.                                      |



 

Pour obtenir l’emplacement du répertoire ProgramData/All Users, appelez la fonction [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) . Le répertoire contient les sous-répertoires suivants :



| Répertoire  | Description                          |
|------------|--------------------------------------|
| Bureau    | Raccourcis à afficher sur le bureau. |
| Menu Démarrer | Éléments de menu du menu **Démarrer** .   |



 

Pour obtenir l’emplacement de l’annuaire de l’utilisateur par défaut, appelez la fonction [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) . Pour obtenir l’emplacement de l’annuaire d’un utilisateur particulier, appelez la fonction [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) . Les répertoires utilisateur par défaut et utilisateurs spécifiques contiennent les sous-répertoires suivants. Les répertoires en italique indiquent les répertoires qui sont masqués par défaut. Vous pouvez afficher ces répertoires en sélectionnant l’option **afficher les fichiers, les dossiers et les lecteurs masqués** dans les **Options des dossiers** , élément du panneau de configuration.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Répertoire</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Données d'application</td>
<td>Données spécifiques à l’application.</td>
</tr>
<tr class="even">
<td>Cookies</td>
<td>Cookies Windows Internet Explorer.</td>
</tr>
<tr class="odd">
<td>Bureau</td>
<td>Raccourcis à afficher sur le bureau.</td>
</tr>
<tr class="even">
<td>Favoris</td>
<td>Liens vers les sites Web favoris.</td>
</tr>
<tr class="odd">
<td>Paramètres locaux</td>
<td>Paramètres et données d’application qui ne sont pas itinérants avec le profil. En général, les paramètres ou les données de ce répertoire sont spécifiques à l’ordinateur ou ils sont trop volumineux pour être itinérants efficacement. Ce répertoire contient les sous-dossiers suivants :
<ul>
<li>Données d'application</li>
<li>Historique</li>
<li>Temp</li>
<li>Fichiers Internet temporaires</li>
</ul></td>
</tr>
<tr class="even">
<td>Mes documents</td>
<td>Emplacement par défaut des documents créés par l’utilisateur. Les applications doivent enregistrer les fichiers de documents dans ce répertoire par défaut.</td>
</tr>
<tr class="odd">
<td><em>Nethotte</em></td>
<td>Raccourcis vers les éléments du voisinage réseau.</td>
</tr>
<tr class="even">
<td><em>PrintHood</em></td>
<td>Raccourcis vers des éléments de dossier d’imprimante.</td>
</tr>
<tr class="odd">
<td><em>Sources</em></td>
<td>Raccourcis vers les documents les plus récemment utilisés.</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>Raccourcis vers les emplacements auxquels l’utilisateur envoie souvent des fichiers.</td>
</tr>
<tr class="odd">
<td>Menu Démarrer</td>
<td>Éléments de menu du menu <strong>Démarrer</strong> .</td>
</tr>
<tr class="even">
<td><em>Modèles</em></td>
<td>Raccourcis vers les éléments de modèle.</td>
</tr>
</tbody>
</table>



 

Pour obtenir l’emplacement des sous-répertoires de ces répertoires, utilisez les fonctions [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ou [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

 

 



