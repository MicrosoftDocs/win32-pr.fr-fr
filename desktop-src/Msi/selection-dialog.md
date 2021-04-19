---
description: Cette boîte de dialogue modale permet aux utilisateurs de sélectionner des éléments particuliers.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Boîte de dialogue de sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539760"
---
# <a name="selection-dialog"></a>Boîte de dialogue de sélection

Cette boîte de dialogue modale permet aux utilisateurs de sélectionner des éléments particuliers.

Une boîte de dialogue de sélection contient un [contrôle SelectionTree](selectiontree-control.md) qui publie plusieurs ControlEvents. En général, ces ControlEvents sont abonnés à des contrôles de [texte](text-control.md), d' [icône](icon-control.md)ou [bitmap](bitmap-control.md) qui affichent une description, la taille, le chemin d’accès et l’icône de l’élément mis en surbrillance.

La boîte de dialogue contient un [contrôle PUSHBUTTON](pushbutton-control.md) qui publie le [ControlEvent, SelectionBrowse](selectionbrowse-controlevent.md) et génère une [boîte de dialogue de navigation](browse-dialog.md). Le contrôle de navigation permet à l’utilisateur de sélectionner un répertoire.

L’arborescence de sélection est remplie uniquement après l’appel de l’action [CostInitialize](costinitialize-action.md) et de l' [action CostFinalize](costfinalize-action.md) .

Une boîte de dialogue de sélection est couramment utilisée pour sélectionner des fonctionnalités. Les fonctionnalités sont répertoriées en tant qu’éléments dans un contrôle SelectionTree et étiquetées avec la chaîne de texte abrégée figurant dans la colonne titre du [tableau des fonctionnalités](feature-table.md). La chaîne de texte dans la colonne Description de la table de fonctionnalités est publiée en tant que [ControlEvent, SelectionDescription](selectiondescription-controlevent.md) et affichée par un [contrôle de texte](text-control.md) dans la boîte de dialogue de sélection. Le contrôle d’arborescence de sélection publie également le handle vers l’icône de l’élément mis en surbrillance.

 

 



