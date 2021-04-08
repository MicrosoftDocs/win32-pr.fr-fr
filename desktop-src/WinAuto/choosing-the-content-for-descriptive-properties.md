---
title: Choix du contenu pour les propriétés descriptives
description: Tandis que le contenu de certaines propriétés est spécifique, le contenu des autres propriétés se compose d’un texte descriptif laissé au développeur du serveur.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729964"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Choix du contenu pour les propriétés descriptives

Tandis que le contenu de certaines propriétés est spécifique, le contenu des autres propriétés se compose d’un texte descriptif laissé au développeur du serveur. En outre, le type d’informations pour chaque propriété varie en fonction de l’objet. Le tableau suivant fournit des suggestions pour le choix du contenu de ces propriétés descriptives.



| Propriété                                        | Suggestion de contenu                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom**](name-property.md)                   | Étiquette qui décrit brièvement et identifie l’objet dans son conteneur, par exemple le texte d’un bouton de commande, le nom d’un élément de menu ou une étiquette affichée à côté d’un contrôle d’édition.                                                                              |
| [**Nœud**](defaultaction-property.md) | Interaction par défaut avec l’objet. La chaîne retournée par cette propriété est soit un verbe unique, tel que « appuyer » pour un bouton de barre d’outils, soit une expression brève qui commence par un verbe.                                                                               |
| [**Valeur**](value-property.md)                 | Informations contenues dans l’objet, telles que le texte d’un contrôle d’édition ou le nom de fichier d’un lien HTML. Le contenu de la propriété [**value**](value-property.md) peut changer, tandis que le contenu de la propriété [**Name**](name-property.md) ne change pas. |
| [**Description**](description-property.md)     | Décrit l’apparence de l’objet.                                                                                                                                                                                                                                    |
| [**Aide**](help-property.md)                   | Info-bulle ou info-bulle utilisées pour décrire ce que fait l’objet ou comment l’utiliser.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Identificateur de contexte d’une rubrique [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) qui documente l’objet.                                                                                                                                                 |



 

Utilisez l’une des valeurs de [rôle d’objet](object-roles.md) prédéfinies pour le [**rôle**](role-property.md) et la combinaison appropriée de [constantes d’état d’objet](object-state-constants.md) pour l' [**État**](state-property.md).

Le contenu des propriétés des contrôles personnalisés doit correspondre au contenu des propriétés des contrôles fournis par le système que les contrôles personnalisés émulent. Pour plus d’informations sur les propriétés prises en charge par les contrôles fournis par le système, consultez [annexe A : informations de référence sur les éléments d’interface utilisateur pris en charge](appendix-a--supported-user-interface-elements-reference.md).

 

 