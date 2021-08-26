---
description: Les auteurs doivent connaître les tables et les champs de la liste suivante lors de la conception de leur interface utilisateur pour être conformes aux instructions de Active Accessibility.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: accessibilité (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8811d47bc7288e966ca5d536b435611c79fd81f3a38fa0b2dbdd422b5939a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078229"
---
# <a name="accessibility-windows-installer"></a>accessibilité (Windows Installer)

Les auteurs doivent connaître les tables et les champs de la liste suivante lors de la conception de leur interface utilisateur pour être conformes aux instructions de Active Accessibility. L’interface utilisateur d’un package d’installation doit faciliter l’accessibilité de l’application ou du produit à tous les utilisateurs.

-   Le texte info-bulle est contenu dans la colonne aide de la [table de contrôle](control-table.md). Ce texte est affiché par les lecteurs d’écran pour les contrôles contenant une image.
-   Le champ de texte de [la table de contrôle](control-table.md) pour les contrôles [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md) et [SelectionTree](selectiontree-control.md) n’est jamais affiché. Au lieu de cela, il peut être lu par les utilitaires de révision d’écran comme description du contrôle. Les personnes qui ne peuvent pas utiliser les informations visuelles sur l’écran peuvent interpréter les informations avec l’aide d’un utilitaire de révision d’écran. Les utilitaires de révision d’écran (également appelés programmes de lecture d’écran ou utilitaires d’accès vocal) prennent les informations affichées à l’écran et les dirigent via un autre support, tel qu’une parole synthétisée ou un affichage braille actualisable.
-   Les contrôles des boîtes de dialogue doivent être liés à l’aide du \_ champ contrôle suivant de la [table de contrôle](control-table.md). Les contrôles doivent être créés de façon à ce qu’ils soient accessibles à l’aide de la touche TAB.
-   Des touches de raccourci doivent être fournies pour accéder directement aux contrôles.
-   La couleur de texte affichée dans l’interface utilisateur est définie dans la [table TextStyle](textstyle-table.md). Si la couleur de texte choisie est trop proche de l’arrière-plan, le choix de couleur du texte est ignoré.
-   La taille et la police du texte sont définies dans la [table TextStyle](textstyle-table.md). Des tailles de police supérieures doivent être utilisées pour les packages destinés au marché asiatique. Par exemple, une taille de police de 10 points lisible pour le texte anglais ne peut pas nécessairement être vraie pour le chinois.
-   Pour les contrôles [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) ou [VolumeSelectCombo](volumeselectcombo-control.md), les lecteurs d’écran prennent accName et accKeyboardShortcut à partir d’un [contrôle de texte](text-control.md) qui doit précéder le contrôle dans la \_ séquence suivante du contrôle de la boîte de dialogue. Le lecteur d’écran prend accName à partir du champ de texte du contrôle de texte et accKeyboardShortcut à partir du raccourci clavier dans le champ de texte, si un raccourci existe.
-   Étant donné que le texte statique ne peut pas prendre le focus, un [contrôle de texte](text-control.md) qui décrit un contrôle [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) ou [VolumeSelectCombo](volumeselectcombo-control.md) doit être rendu en premier contrôle dans la boîte de dialogue pour garantir la compatibilité avec les lecteurs d’écran.
-   Pour un [contrôle PUSHBUTTON](pushbutton-control.md) qui affiche une icône ou une image bitmap, AccName et accKeyboardShortcut sont spécifiés dans le champ d’aide de l’enregistrement de la [table de contrôle](control-table.md) , à gauche du \| séparateur.
-   Évitez d’utiliser des contrôles de texte sur des bitmaps blanches, car sous contraste élevé noir le texte peut devenir invisible.
-   N’ajoutez pas de contrôle de texte noir sur un arrière-plan qui est une image bitmap blanche. ce texte n’est pas visible à l’utilisateur qui modifie l’affichage du Windows en contraste élevé noir.
-   N’ajoutez pas de contrôle de texte blanc sur un arrière-plan qui est une image bitmap noire. ce texte n’est pas visible à l’utilisateur qui modifie l’affichage du Windows en contraste élevé blanc.
-   Ne placez pas de [contrôles de texte](text-control.md) transparent par-dessus les bitmaps de couleur. Le texte peut ne pas être visible si l’utilisateur modifie le modèle de couleurs d’affichage. Par exemple, le texte peut devenir invisible si l’utilisateur définit le paramètre de contraste élevé pour l’accessibilité.
-   Notez que le focus sur une boîte de dialogue ne fait pas la tabulation d’un [contrôle RadioButtonGroup](radiobuttongroup-control.md) tant que l’un des boutons du groupe n’a pas été sélectionné. Pour définir l’onglet focus sur ce groupe de boutons, spécifiez l’un des boutons comme paramètre par défaut pour le contrôle.
-   Pour fournir aux programmes de lecture d’écran un texte descriptif supplémentaire sur un [contrôle RadioButtonGroup](radiobuttongroup-control.md). Suivez l’exemple fourni dans [Ajout de texte supplémentaire aux cases d’option](adding-extra-text-to-radio-buttons.md).
-   La taille relative des boîtes de dialogue, contrôles et polices peut varier en fonction de la taille de police choisie. Pour plus d’informations, consultez [unités d’installation](installer-units.md). Pour garantir un affichage correct du texte et des contrôles dans l’interface utilisateur, les développeurs du programme d’installation doivent toujours tester leur application à l’aide de toutes les tailles de police qui peuvent être utilisées.

 

 



