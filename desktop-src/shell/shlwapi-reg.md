---
description: cette section décrit les fonctions de gestion du registre Windows Shell. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion du Registre Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8a3e4f65904fa97635b3ef4dc3abd9f01344f6a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412323"
---
# <a name="shell-registry-handling-functions"></a>Fonctions de gestion du Registre Shell

cette section décrit les fonctions de gestion du registre Windows Shell. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                             | Description                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Retourne un pointeur vers un objet [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Récupère le type perçu d’un fichier en fonction de son extension.<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Détermine si un type de fichier est considéré comme un risque potentiel pour la sécurité.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Recherche et récupère une clé associée à un fichier ou une association de protocole à partir du Registre.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Recherche et récupère une chaîne associée à un fichier ou une association de protocole à partir du Registre.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Recherche et récupère une chaîne associée à une association de fichiers à partir du Registre à partir d’une clé spécifiée.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Copie de manière récursive les sous-clés et les valeurs de la sous-clé source vers la clé de destination. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) ne copie pas les attributs de sécurité des clés.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Supprime une clé vide.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Supprime une sous-clé et tous ses descendants. Cette fonction supprime la clé et toutes les valeurs de la clé du Registre.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Supprime une valeur nommée de la clé de Registre spécifiée.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Énumère les sous-clés de la clé de Registre ouverte spécifiée.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Énumère les valeurs de la clé de Registre ouverte spécifiée.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Récupère un tableau de sous-clés de classe associées à un objet [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Récupère une valeur de registre.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Ouvre une valeur de Registre et fournit un flux qui peut être utilisé pour lire ou écrire dans la valeur. Cette fonction remplace [**SHOpenRegStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama).<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Récupère des informations sur une clé de Registre spécifiée.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Ouvre une clé de Registre et l’interroge pour obtenir une valeur spécifique.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Ferme un handle vers une sous-clé de Registre spécifique à l’utilisateur dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Crée ou ouvre une sous-clé de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Supprime une sous-arborescence de Registre vide d’une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Supprime une valeur de sous-clé de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Duplique le handle HKEY d’une clé de registre.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Énumère les sous-clés d’une sous-clé de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Énumère les valeurs de la sous-clé de Registre spécifiée dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Récupère une valeur booléenne d’une sous-arborescence de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Lit une valeur de chaîne numérique à partir du Registre et la convertit en entier.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Récupère un chemin d’accès au fichier à partir du Registre, en développant les variables d’environnement en fonction des besoins.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Récupère une valeur d’une sous-arborescence de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Ouvre une sous-arborescence de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Récupère des informations sur une sous-clé de Registre spécifiée dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Récupère le type et les données pour un nom spécifié associé à une sous-clé Open Registry dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Prend un chemin d’accès de fichier, remplace les noms de dossiers par des chaînes d’environnement et place la chaîne résultante dans le registre.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Définit une valeur de sous-clé de Registre dans une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Définit une valeur de registre.<br/> Utilisez [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) à la place.<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Écrit une valeur dans une sous-clé de registre d’une sous-arborescence spécifique à l’utilisateur (HKEY \_ Current \_ User ou HKEY \_ local \_ machine).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Définit la valeur d’une clé de registre.<br/>                                                                                                                                        |



 

 

 
