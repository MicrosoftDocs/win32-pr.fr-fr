---
description: L’interpréteur de commandes utilise une sous-clé de Registre ProgID (identificateur programmatique) pour associer un type de fichier à une application et contrôler le comportement de l’Association.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificateurs programmatiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991077"
---
# <a name="programmatic-identifiers"></a>Identificateurs programmatiques

L’interpréteur de commandes utilise une sous-clé de Registre ProgID (identificateur programmatique) pour associer un type de fichier à une application et contrôler le comportement de l’Association. Les entrées ProgID utilisées pour les associations de fichiers se trouvent sous la **\_ \_ racine de classes HKEY** dans le registre.

Cette rubrique est organisée comme suit :

-   [Éléments d’identificateur programmatique utilisés par les associations de fichiers](#programmatic-identifier-elements-used-by-file-associations)
-   [Utilisation d’identificateurs programmatiques avec version](#using-versioned-programmatic-identifiers)
-   [Rubriques connexes](#related-topics)

Pour plus d’informations, consultez [comment inscrire un type de fichier pour une nouvelle application](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Éléments d’identificateur programmatique utilisés par les associations de fichiers

Le format approprié d’un nom de clé ProgID est \[ *Vendor ou application* \] . \[ *Composant* \] . \[  \] , Séparées par des points et sans espaces, comme dans Word.Document. 6. La partie *version* est facultative, mais vivement recommandée. Pour plus d’informations, consultez [utilisation d’identificateurs programmatiques avec version](#using-versioned-programmatic-identifiers).

Une sous-clé ProgID doit inclure les éléments suivants. Notez que certaines données de chaîne de cette clé requièrent une mise en forme spécifique.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Valeurs</strong></td>
<td>Définissez l’entrée par défaut de la sous-clé ProgID sur un nom convivial pour ce ProgID, pouvant être affiché à l’utilisateur. L’utilisation de cette entrée pour contenir le nom convivial est déconseillée par l’entrée FriendlyTypeName sur les systèmes exécutant Windows 2000 ou une version ultérieure. Toutefois, vous devez définir cette valeur pour la compatibilité descendante.<br/></td>
</tr>
<tr class="even">
<td><strong>AllowSilentDefaultTakeOver</strong> (introduit dans Windows 8)</td>
<td>Définissez cette entrée facultative pour signaler que Windows doit ignorer ce ProgID lors de la détermination d’un gestionnaire par défaut pour un type de fichier public. Que cette valeur soit définie ou non, l’identificateur de programme (ProgID) continue à s’afficher dans le menu contextuel et la boîte de dialogue OpenWith. Il s’agit d’une valeur REG_NONE.</td>
</tr>
<tr class="odd">
<td><strong>AppUserModelID</strong> (introduite dans Windows 7)</td>
<td>Définissez cette entrée facultative sur l’ID de modèle utilisateur d’application explicite de l’application (AppUserModelID) si l’application utilise une valeur AppUserModelID explicite et utilise les listes de raccourcis <strong>récentes</strong> ou <strong>fréquentes</strong> générées par le système, ou fournit une liste de raccourcis personnalisée. Si une application utilise un AppUserModelID explicite et ne définit pas cette valeur, les éléments ne s’affichent pas dans les listes de raccourcis de cette application. Il s’agit d’une chaîne de REG_SZ. Pour plus d’informations, consultez <a href="appids.md">ID de modèle d’utilisateur d’application (AppUserModelIDs)</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>Définissez cette entrée facultative à l’aide d’indicateurs à partir de l’énumération <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> . L’entrée indicateurs contrôle certains aspects de la gestion de l’interpréteur de commandes des types de fichiers liés à ce ProgID. Vous pouvez également utiliser l’entrée indicateurs pour limiter la capacité de l’utilisateur à modifier certains aspects de ces types de fichiers à l’aide de la feuille de propriétés d’un fichier. Les valeurs <strong>FILETYPEATTRIBUTEFLAGS</strong> utilisées pour indicateurs sont des valeurs binaires conçues pour vous permettre de combiner plusieurs attributs en une seule valeur dans une opération or au niveau du bit. Il s’agit d’une valeur REG_DWORD ou REG_BINARY.<br/></td>
</tr>
<tr class="odd">
<td><strong>FriendlyTypeName</strong></td>
<td>Définissez cette entrée sur un nom convivial pour le ProgID, pouvant être affiché à l’utilisateur. Pour des fins de cohérence, cette chaîne doit contenir les mêmes données que l’entrée par défaut pour cette clé ProgID. Cette entrée peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais elle doit être formatée comme une chaîne indirecte (nom de fichier complet et valeur de ressource précédée du symbole @), par exemple <em>@% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>Définissez cette entrée sur un bref message d’aide que l’interpréteur de commandes affiche pour ce ProgID. L’entrée info-bulle s’affiche dans une boîte de dialogue de pointage avec la souris. Cette valeur peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais comme FriendlyTypeName, elle doit être mise en forme en tant que chaîne indirecte.<br/></td>
</tr>
<tr class="odd">
<td><strong>CurVer</strong></td>
<td>Définissez l’entrée (par défaut) de cette sous-clé sur la version la plus récente de ce ProgID.<br/>
<blockquote>
[!Note]<br />
À moins que vous n’ayez des versions d’application côte à côte, autrement dit, si plusieurs versions sont installées sur le même système, vous devez éviter d’utiliser <strong>Curver</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>.</td>
<td>Définissez l’entrée (par défaut) de cette sous-clé sur l’icône par défaut que vous souhaitez afficher pour les types de fichiers associés à ce ProgID. Cette valeur peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais elle doit être fournie sous la forme d’un nom de fichier complet avec sa valeur de ressource de surveillance, par exemple <em>% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
</tbody>
</table>



 

L’exemple de clé de Registre suivant illustre un nœud de clé ProgID d’association de fichiers :

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Utilisation d’identificateurs programmatiques avec version

Un ProgID avec version est un ProgID dont la version est indiquée dans son nom. Pour ce faire, vous devez ajouter un point et le numéro de version au nom. Par exemple :

-   Word.Document. 6
-   Word.Document. 8

Il s’agit de ProgID avec version, respectivement les versions 6 et 8. Si vous disposez d’une application côte à côte, autrement dit, une application qui prend en charge plusieurs versions de votre application installées en même temps, utilisez des ProgID indépendants de la version et de CurVer. Dans le cas contraire, vous devez éviter les ProgID indépendants de la version et de CurVer, car ils risquent d’être inefficaces.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment inscrire un type de fichier pour une nouvelle application](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 




