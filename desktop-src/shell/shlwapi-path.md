---
description: Cette section décrit les fonctions de gestion du chemin d’accès de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion du chemin de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991760"
---
# <a name="shell-path-handling-functions"></a>Fonctions de gestion du chemin de Shell

Cette section décrit les fonctions de gestion du chemin d’accès de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br/></td>
<td>Ajoute une barre oblique inverse à la fin d’une chaîne pour créer la syntaxe correcte pour un chemin d’accès. Si le chemin d’accès source contient déjà une barre oblique inverse de fin, aucune barre oblique inverse n’est ajoutée. <br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br/></td>
<td>Ajoute une extension de nom de fichier à une chaîne de chemin d’accès.<br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br/></td>
<td>Ajoute un chemin d’accès à la fin d’un autre. <br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br/></td>
<td>Crée un chemin d’accès racine à partir d’un numéro de lecteur donné.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a><br/></td>
<td>Simplifie un tracé en supprimant des éléments de navigation tels que &quot; . &quot; et &quot; .. &quot; pour produire un chemin d’accès direct et correctement formé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br/></td>
<td>Concatène deux chaînes qui représentent les chemins d’accès formés correctement dans un chemin d’accès ; concatène également tous les éléments de chemin d’accès relatifs. <br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br/></td>
<td>Compare deux chemins d’accès pour déterminer s’ils partagent un préfixe commun. Un préfixe est l’un des types suivants : &quot; C : \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br/></td>
<td>Tronque un chemin d’accès de fichier pour qu’il s’ajuste à une largeur de pixel donnée en remplaçant les composants de tracé par des ellipses.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br/></td>
<td>Tronque un tracé pour qu’il s’ajuste à un certain nombre de caractères en remplaçant les composants du tracé par des ellipses.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br/></td>
<td>Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br/></td>
<td>Crée un chemin d’accès à partir d’une URL de fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br/></td>
<td>Détermine si un chemin d’accès à un objet de système de fichiers, tel qu’un fichier ou un dossier, est valide.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br/></td>
<td>Recherche une extension dans un chemin d’accès.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br/></td>
<td>Recherche un nom de fichier dans un chemin d’accès.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br/></td>
<td>Analyse un chemin d’accès et retourne la partie de ce chemin d’accès qui suit la première barre oblique inverse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br/></td>
<td>Recherche un fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br/></td>
<td>Détermine si un nom de fichier donné a une liste de suffixes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br/></td>
<td>Recherche les arguments de ligne de commande dans un chemin d’accès donné.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br/></td>
<td>Détermine le type de caractère par rapport à un chemin d’accès.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br/></td>
<td>Recherche dans un chemin d’accès une lettre de lecteur comprise entre « A » et « Z » et retourne le numéro de lecteur correspondant.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br/></td>
<td>Détermine si le type de contenu inscrit d’un fichier correspond au type de contenu spécifié. Cette fonction obtient le type de contenu pour le type de fichier spécifié et compare cette chaîne avec le <em>pszContentType</em>. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br/></td>
<td>Vérifie qu’un chemin d’accès est un répertoire valide.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br/></td>
<td>Détermine si un chemin d’accès spécifié est un répertoire vide.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br/></td>
<td>Recherche un chemin d’accès pour tous les caractères délimitant les chemins d’accès (par exemple, ' : 'ou' \' ). Si aucun caractère de délimitation de chemin d’accès n’est présent, le chemin d’accès est considéré comme un chemin d’accès de spécifications de fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br/></td>
<td>Détermine si un fichier est un fichier HTML. La détermination est effectuée en fonction du type de contenu inscrit pour l’extension du fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br/></td>
<td>Détermine si un nom de fichier est au format long.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br/></td>
<td>Détermine si une chaîne de chemin d’accès représente une ressource réseau.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br/></td>
<td>Recherche un chemin d’accès pour déterminer s’il contient un préfixe valide du type passé par <em>pszPrefix</em>. Un préfixe est l’un des types suivants : &quot; C : \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br/></td>
<td>Recherche un chemin d’accès et détermine s’il est relatif.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br/></td>
<td>Détermine si une chaîne de chemin d’accès fait référence à la racine d’un volume.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br/></td>
<td>Compare deux chemins d’accès pour déterminer s’ils ont un composant racine commun.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br/></td>
<td>Détermine si un dossier existant contient les attributs qui en font un dossier système. Cette fonction indique également si certains attributs qualifient un dossier comme dossier système.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br/></td>
<td>Détermine si une chaîne de chemin d’accès est un chemin d’accès UNC (Universal Naming Convention) valide, par opposition à un chemin d’accès basé sur une lettre de lecteur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br/></td>
<td>Détermine si une chaîne est un UNC valide pour un chemin d’accès de serveur uniquement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br/></td>
<td>Détermine si une chaîne est un chemin d’accès de partage UNC valide, un partage de \\ <em>serveur</em> \ <em></em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br/></td>
<td>Teste une chaîne donnée pour déterminer si elle est conforme à un format d’URL valide.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br/></td>
<td>Convertit un chemin tout en majuscules en caractères minuscules pour que le chemin d’accès soit une apparence cohérente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br/></td>
<td>Donne à un dossier existant les attributs appropriés pour devenir un dossier système.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br/></td>
<td>Recherche une chaîne à l’aide d’un type de correspondance de caractère générique MS-DOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br/></td>
<td>Correspond à un nom de fichier à partir d’un chemin d’accès par rapport à un ou plusieurs modèles de nom de fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br/></td>
<td>Analyse une chaîne d’emplacement de fichier qui contient un emplacement de fichier et un index d’icône, et retourne des valeurs distinctes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br/></td>
<td>Recherche des espaces dans un chemin d’accès. Si des espaces sont trouvés, le chemin d’accès entier est placé entre guillemets.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br/></td>
<td>Crée un chemin d’accès relatif d’un fichier ou dossier à un autre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br/></td>
<td>Supprime tous les arguments d’un chemin d’accès donné.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br/></td>
<td>Supprime la barre oblique inverse de fin d’un chemin d’accès donné.<br/>
<blockquote>
[!Note]<br />
Cette fonction est déconseillée. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> à la place.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br/></td>
<td>Supprime tous les espaces de début et de fin d’une chaîne.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br/></td>
<td>Supprime l’extension de nom de fichier d’un chemin d’accès, si celle-ci est présente. <br/>
<blockquote>
[!Note]<br />
Cette fonction est déconseillée. Nous vous recommandons d’utiliser <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> à la place.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br/></td>
<td>Supprime le nom de fichier de fin et la barre oblique inverse d’un chemin d’accès, s’ils sont présents.<br/>
<blockquote>
[!Note]<br />
Cette fonction est déconseillée. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> à la place.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br/></td>
<td>Remplace l’extension d’un nom de fichier par une nouvelle extension. Si le nom de fichier ne contient pas d’extension, l’extension est attachée à la fin de la chaîne.<br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br/></td>
<td>Détermine si un chemin d’accès donné est correctement mis en forme et complet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br/></td>
<td>Définit le texte d’un contrôle enfant dans une fenêtre ou une boîte de dialogue, à l’aide de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> pour garantir que le chemin d’accès est ajusté dans le contrôle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br/></td>
<td>Récupère un pointeur désignant le premier caractère d’un chemin d’accès qui suit les éléments de lettre de lecteur ou de chemin d’accès de partage/serveur UNC.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br/></td>
<td>Supprime la partie chemin d’accès d’un fichier et d’un chemin d’accès qualifiés complets.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br/></td>
<td>Supprime tous les éléments de fichier et de répertoire dans un chemin d’accès à l’exception des informations de racine.<br/>
<blockquote>
[!Note]<br />
Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon. Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> plus sûre à la place.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br/></td>
<td>Supprime la décoration d’une chaîne de chemin d’accès.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br/></td>
<td>Remplace certains noms de dossiers dans un chemin d’accès qualifié complet par la chaîne d’environnement qui leur est associée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br/></td>
<td>Supprime les attributs d’un dossier qui en fait un dossier système. Ce dossier doit réellement exister dans le système de fichiers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br/></td>
<td>Supprime les guillemets à partir du début et de la fin d’un chemin d’accès.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br/></td>
<td>Vérifie un contexte de liaison pour voir s’il est possible de lier en toute sécurité à un objet de composant particulier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br/></td>
<td>Détermine un schéma pour une chaîne d’URL spécifiée et retourne une chaîne avec un préfixe approprié.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br/></td>
<td>Convertit une chaîne d’URL en forme canonique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br/></td>
<td>Lorsqu’il est fourni avec une URL relative et sa base, retourne une URL sous forme canonique.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br/></td>
<td>Effectue une comparaison sensible à la casse de deux chaînes d’URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br/></td>
<td>Convertit un chemin d’accès MS-DOS en URL canonique.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br/></td>
<td>Convertit des caractères ou des paires de substitution dans une URL qui peuvent être modifiées pendant le transport sur Internet ( &quot; caractères non sécurisés &quot; ) en leurs séquences d’échappement correspondantes. Les paires de substitution sont des caractères compris entre U + 10000 et U + 10FFFF (au format UTF-32) ou entre DC00 et et DFFF (UTF-16). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br/></td>
<td>Macro qui convertit les espaces en séquence d’échappement correspondante.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br/></td>
<td>Récupère l’emplacement à partir d’une URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br/></td>
<td>Accepte une chaîne d’URL et retourne une partie spécifiée de cette URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br/></td>
<td>Hache une chaîne d’URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a><br/></td>
<td>Teste si une URL est un type spécifié.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br/></td>
<td>Teste une URL pour déterminer s’il s’agit d’une URL de fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br/></td>
<td>Retourne une valeur indiquant si une URL est une URL que les navigateurs n’incluent généralement pas dans l’historique de navigation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br/></td>
<td>Retourne une valeur indiquant si une URL est opaque.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br/></td>
<td>Convertit les séquences d’échappement en caractères ordinaires.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br/></td>
<td>Convertit les séquences d’échappement en caractères ordinaires et remplace la chaîne d’origine.<br/></td>
</tr>
</tbody>
</table>



 

 

 




