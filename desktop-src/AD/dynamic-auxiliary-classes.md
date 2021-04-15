---
title: Classes auxiliaires dynamiques
description: À l’instar des classes d’objets structurelles et abstraites, les classes auxiliaires sont définies par un objet classSchema dans le schéma Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462875"
---
# <a name="dynamic-auxiliary-classes"></a>Classes auxiliaires dynamiques

À l’instar des classes d’objets structurelles et abstraites, les classes auxiliaires sont définies par un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) dans le schéma Active Directory. Pour plus d’informations, consultez [classes structurelles, abstraites et auxiliaires](structural-abstract-and-auxiliary-classes.md). Cette définition de schéma spécifie différentes caractéristiques de la classe, y compris les attributs associés à la classe.

Contrairement aux classes structurelles, vous ne pouvez pas créer une instance d’une classe auxiliaire comme vous pouvez le faire avec une classe structurelle. Au lieu de cela, vous utilisez une classe auxiliaire pour étendre la liste des attributs qui est associée à une autre classe d’objets structurelle, abstraite ou auxiliaire.

Dans la version initiale de Windows 2000, Active Directory Domain Services fourni la prise en charge de la liaison statique des classes auxiliaires à la définition [**classSchema**](/windows/desktop/ADSchema/c-classschema) d’une autre classe d’objets. Quand une classe auxiliaire est utilisée de cette façon, chaque instance de la classe d’objet prend en charge les attributs de la classe auxiliaire.

**Windows 2000 Server et versions antérieures :** Active Directory Domain Services ne prend pas en charge la liaison dynamique des classes auxiliaires à des objets individuels, et pas seulement à des classes entières d’objets. En outre, les classes auxiliaires qui ont été attachées à une instance d’objet ne peuvent pas être supprimées par la suite de l’instance.

**Windows Server 2003 :** Les classes auxiliaires dynamiques sont prises en charge lorsque tous les contrôleurs de domaine de la forêt exécutent Windows Server 2003 et le mode fonctionnel de la forêt est Windows Server 2003.

Pour plus d’informations sur les classes auxiliaires, consultez :

-   [Classes auxiliaires liées de manière dynamique](dynamically-linked-auxiliary-classes.md)
-   [Classes auxiliaires liées statiquement](statically-linked-auxiliary-classes.md)
-   [Détermination des classes associées à une instance d’objet](determining-the-classes-associated-with-an-object-instance.md)
-   [Ajout d’une classe auxiliaire à une instance d’objet](adding-an-auxiliary-class-to-an-object-instance.md)

Pour plus d’informations sur les niveaux fonctionnels de forêt, consultez la rubrique « Comment élever Active Directory niveaux fonctionnels de domaine et de forêt » dans la base de connaissances de l’aide et du support à l’adresse [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 