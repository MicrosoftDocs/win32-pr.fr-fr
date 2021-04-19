---
description: Pour chaque mot de passe qui doit être entré par l’utilisateur, ajoutez un contrôle d’édition sur une boîte de dialogue qui stocke la valeur du mot de passe dans une propriété.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Création de l’interface utilisateur pour l’entrée de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518650"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Création de l’interface utilisateur pour l’entrée de mot de passe

Pour chaque mot de passe qui doit être entré par l’utilisateur, ajoutez un contrôle d’édition sur une boîte de dialogue qui stocke la valeur du mot de passe dans une propriété. Ce [contrôle d’édition](edit-control.md) doit avoir l' [attribut de contrôle de mot de passe](password-control-attribute.md). Cela spécifie que la propriété entrée est un mot de passe et empêche le programme d’installation d’écrire la propriété dans le fichier journal.

Les [attributs de contrôle](control-attributes.md) du contrôle de modification de mot de passe sont MsidbControlAttributesVisible, MsidbControlAttributesEnabled et msidbControlAttributesPasswordInput (1 + 2 + 2097152). Les cases X, Y, largeur, hauteur et contrôle \_ dépendent de la disposition du contrôle dans la boîte de dialogue.

[Table de contrôle](control-table.md)



| Dialogue\_ | contrôle\_            | Type | X   | O   | Largeur | Hauteur | Attributs | Propriété         | Texte | Contrôle \_ suivant | Aide |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Modifier | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Annuler        |      |



 

Continuez à [sécuriser l’installation](securing-the-installation.md).

 

 



