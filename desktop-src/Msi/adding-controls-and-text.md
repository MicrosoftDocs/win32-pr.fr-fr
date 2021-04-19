---
description: Les contrôles et le texte placés dans les boîtes de dialogue et les panneaux permettent à l’utilisateur d’interagir avec le processus d’installation.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Ajout de contrôles et de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518654"
---
# <a name="adding-controls-and-text"></a>Ajout de contrôles et de texte

Les contrôles et le texte placés dans les boîtes de dialogue et les panneaux permettent à l’utilisateur d’interagir avec le processus d’installation. Ajoutez une boîte de dialogue à l’interface utilisateur en l’incluant dans la [table de boîte de dialogue](dialog-table.md) , comme décrit dans utilisation de [l’interface utilisateur](using-the-user-interface.md). Remplissez les boîtes de dialogue et les panneaux avec les contrôles en remplissant respectivement la table de [contrôle](control-table.md) et la [table BBControl](bbcontrol-table.md).

Les attributs de contrôle initiaux peuvent être spécifiés dans la colonne attributs de la [table de contrôle](control-table.md). Consultez [attributs du contrôle](control-attributes.md).

Pour rendre les attributs de contrôle dépendants d’une condition, utilisez la [table ControlCondition](controlcondition-table.md) pour désactiver, activer, masquer ou afficher un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle. Vous pouvez également utiliser ce tableau pour remplacer la spécification du contrôle par défaut entré dans la [table de boîtes de dialogue](dialog-table.md).

Pour qu’un événement change un attribut de contrôle, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md). Un ControlEvent, spécifie une action à entreprendre par le programme d’installation ou une modification des attributs d’un ou plusieurs contrôles dans la boîte de dialogue. Consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md). Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de ControlEvent, dans la colonne d’événement de la [table EventMapping](eventmapping-table.md).

Certains contrôles facilitent la collecte d’informations auprès de l’utilisateur. Par exemple, une case à cocher permet à l’utilisateur de définir la valeur d’une propriété. Consultez la table de [cases à cocher](checkbox-table.md), la table de [zone de liste modifiable](combobox-table.md), la table [ListBox](listbox-table.md), la [table RadioButton](radiobutton-table.md)et la [table ListView](listview-table.md).

Notez que, pour des raisons de sécurité, les propriétés privées ne peuvent pas être modifiées par l’utilisateur qui interagit avec l’interface utilisateur. Si une propriété doit être définie par l’interface utilisateur, elle doit être une propriété publique et avoir un nom en majuscules. Consultez [à propos des propriétés](about-properties.md).

Vous pouvez faire en sorte que votre boîte de dialogue présente des informations à l’utilisateur ou l’écrire dans un journal en réponse aux actions d’installation en remplissant la [table ActionText](actiontext-table.md).

Les contrôles peuvent avoir un style de police prédéfini. Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&*style*} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée.

Il est recommandé que la propriété [**DefaultUIFont**](defaultuifont.md) de chaque package d’installation avec une interface utilisateur soit définie dans la [table des propriétés](property-table.md) avec l’un des styles prédéfinis listés dans le [tableau TextStyle](textstyle-table.md). Si cette propriété n’est pas spécifiée, le programme d’installation utilise la police système. Cela peut entraîner l’affichage incorrect des chaînes de texte par le programme d’installation si la page de codes du package est différente de la page de codes de l’interface utilisateur par défaut de l’utilisateur.

Pour la plupart des contrôles, le texte est affiché à l’aide du jeu de caractères spécifié par la page de codes de la base de données. Cela permet de s’assurer que le jeu de caractères correct est utilisé avec les informations contenues dans la base de données. Les exceptions sont les contrôles [Edit](edit-control.md), [DirectoryList](directorylist-control.md), [PathEdit](pathedit-control.md)et [DirectoryCombo](directorycombo-control.md) , qui affichent toujours du texte à l’aide du jeu de caractères de l’interface utilisateur par défaut de l’utilisateur. Les contrôles [Text](text-control.md), [ListBox](listbox-control.md)et [ComboBox](combobox-control.md) utilisent le jeu de caractères de l’interface utilisateur par défaut de l’utilisateur si l' [attribut de contrôle UsersLanguage](userslanguage-control-attribute.md) est défini.

Dans certains cas, un contrôle peut être redessiné de manière incorrecte lors de l’annulation d’une boîte de dialogue. Cela s’effectue avec l’ordre dans lequel les contrôles reçoivent des \_ messages WM Paint après la suppression de la boîte de dialogue **Annuler** . Pour résoudre ce problème, essayez de modifier l’ordre des contrôles dans la table de contrôle.

Les contrôles doivent être suffisamment grands pour accueillir l’intégralité du texte affiché dans tous les paramètres de taille de police. Les contrôles doivent être suffisamment grands pour accueillir l’intégralité du texte localisé, si le texte de l’interface utilisateur peut être localisé. Les tailles de police supérieures ou le texte localisé peuvent nécessiter plus d’espace que le texte d’origine et peuvent être tronqués par un contrôle qui est rendu trop petit. Pour plus d’informations sur la localisation du texte de l’interface utilisateur, consultez la section [exemple de localisation](a-localization-example.md).

 

 



