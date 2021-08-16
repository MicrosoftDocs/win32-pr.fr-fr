---
description: Une boîte de dialogue Parcourir permet à l’utilisateur de sélectionner un répertoire. Le répertoire n’a pas besoin d’exister et peut être créé à l’aide de ce contrôle.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Boîte de dialogue Parcourir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7caceb8e10bc99a9edd8fa5b828efa2e5cbc8b4ed7164d40e2235e19c098199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380711"
---
# <a name="browse-dialog"></a>Boîte de dialogue Parcourir

Une boîte de dialogue Parcourir permet à l’utilisateur de sélectionner un répertoire. Le répertoire n’a pas besoin d’exister et peut être créé à l’aide de ce contrôle.

Ce type de boîte de dialogue contient généralement les trois contrôles suivants. Ces contrôles sont connectés à la même propriété. Cette propriété est le chemin d’accès sélectionné.

-   [Contrôle PathEdit](pathedit-control.md) pour sélectionner la section de fin du chemin d’accès. Ce contrôle ne peut pas perdre le focus si la fin entrée n’est pas valide sur le volume présent.
-   [Contrôle DirectoryCombo](directorycombo-control.md) pour afficher le chemin d’accès actuellement sélectionné qui est affiché par le contrôle PathEdit. Ce contrôle n’affiche pas le dernier segment du chemin d’accès.
-   [Contrôle DirectoryList](directorylist-control.md) pour afficher les dossiers situés sous le répertoire actuellement affiché par le DirectoryCombo. Cela peut également indiquer un dossier qui n’a pas encore été créé.

Une boîte de dialogue de navigation contient généralement un [contrôle DirectoryCombo](directorycombo-control.md) qui spécifie les types de volumes à afficher. Il est courant que tous les types de volumes s’affichent dans une boîte de dialogue de navigation.

Les boîtes de dialogue de navigation contiennent généralement trois [contrôles PUSHBUTTON](pushbutton-control.md). Ces boutons sont liés à leur ControlEvents respectif dans la [table ControlEvent,](controlevent-table.md). Ces boutons sont utilisés pour activer les options de contrôle suivantes.



| Option de contrôle | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Dossier parent   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nouveau dossier     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Ouvrir           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Pour que l’option nouveau dossier fonctionne avec un nom de dossier autre que celui par défaut, le chemin d’accès du nouveau dossier doit être spécifié dans la [table UIText](uitext-table.md). La chaîne de chemin d’accès doit utiliser le \| format « nom de fichier long du nom de fichier long » pour le nom de fichier. Par exemple, utilisez un nom de fichier tel que « MyProd ~ 1 \| My merveilleuse Product ». Pour plus d’informations sur le format de nom de fichier, consultez type de données de la colonne [filename](filename.md) . Si le chemin d’accès n’est pas présent dans la table UIText, ou s’il est défini sur une valeur non valide, la valeur par défaut est « FLDR \| New Folder ». Le bouton **nouveau dossier** peut être omis si la boîte de dialogue ne doit rechercher que des dossiers existants.

 

 



