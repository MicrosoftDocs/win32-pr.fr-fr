---
description: Windows Le programme d’installation de contient des fonctionnalités qui permettent aux développeurs de packages d’installation de créer une interface utilisateur graphique (GUI) qui est présentée à l’utilisateur final lors de l’installation.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: À propos de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092926"
---
# <a name="about-the-user-interface"></a>À propos de l’interface utilisateur

Windows Le programme d’installation de contient des fonctionnalités qui permettent aux développeurs de packages d’installation de créer une interface utilisateur graphique (GUI) qui est présentée à l’utilisateur final lors de l’installation. Cette interface utilisateur peut présenter le comportement de l' [Assistant interface utilisateur](user-interface-wizard-behavior.md), afficher des boîtes de dialogue et des panneaux, et présenter des contrôles interactifs aux utilisateurs pendant l’installation.

l’interface utilisateur interne du programme d’installation est gérée et contrôlée via un ensemble de tables de base de données dans Windows Installer elles-mêmes. Le programme d’installation fournit uniquement un petit ensemble de boîtes de dialogue par défaut destinées à gérer les messages d’erreur et d’information. Toutes les boîtes de dialogue personnalisées doivent être créées par l’auteur du package.

il n’existe aucune API Windows Installer spécifique pour permettre à un auteur de package de créer une interface utilisateur par programme. il est possible d’utiliser l’API Microsoft Windows pour créer une interface utilisateur par programmation. Toutefois, il est recommandé que les auteurs de package utilisent l’interface utilisateur interne fournie.

Les auteurs du package d’installation créent des boîtes de dialogue personnalisées en entrant le nom de leur boîte de dialogue personnalisée dans la \_ colonne « boîte de dialogue » de la table de boîte de dialogue et en spécifiant la taille, la position et d’autres attributs à l’aide des autres colonnes.

Windows Le programme d’installation implémente également un certain nombre de contrôles standard que l’auteur d’un package peut placer dans des boîtes de dialogue. les contrôles Microsoft Windows standard ne sont pas tous disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.

Pour créer des contrôles dans une boîte de dialogue spécifique, entrez le nom de la boîte de dialogue, la clé primaire de l’entrée de la boîte de dialogue dans la table de boîte de dialogue, le deuxième champ de la table de contrôle et spécifiez la taille, la position et d’autres attributs du contrôle à l’aide des colonnes restantes.

Les contrôles actifs doivent être liés à un ControlEvent, dans la [table ControlEvent,](controlevent-table.md) pour permettre l’interaction de l’utilisateur avec l’installation. Les contrôles passifs qui reçoivent et affichent des informations doivent être abonnés à un ControlEvent, approprié dans la [table EventMapping](eventmapping-table.md).

Pour plus d’informations sur ControlEvents, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md). Notez qu’un contrôle publie un ControlEvent, s’il est listé dans la table ControlEvent, et s’abonne à un événement, s’il est listé dans la table EventMapping.

L’affichage de l’interface utilisateur du programme d’installation au cours de l’installation est géré via les tables de séquences d’interface utilisateur : [InstallUISequence table](installuisequence-table.md)et [AdminUISequence table](adminuisequence-table.md). L’une de ces tables de séquences est exécutée en fonction de l’action de niveau supérieur qui a initié l’installation : [install](install-action.md), [admin](admin-action.md)ou [advertise](advertise-action.md).

pour plus d’informations sur l’implémentation d’une interface utilisateur dans Windows Installer, consultez [utilisation de l’interface utilisateur](using-the-user-interface.md), [schéma d’interface utilisateur](user-interface-schema.md), ainsi que les rubriques individuelles pour les boîtes de dialogue et les contrôles.

 

 



