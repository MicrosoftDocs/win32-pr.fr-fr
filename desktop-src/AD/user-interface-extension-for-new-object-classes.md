---
title: Extension de l’interface utilisateur pour les nouvelles classes d’objets
description: Active Directory Domain Services et son interface utilisateur du composant logiciel enfichable MMC d’administration peuvent être personnalisés pour s’adapter aux besoins des administrateurs et des utilisateurs.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Extension de l’interface utilisateur pour les nouvelles classes d’objets AD
- Object AD, extension de l’interface utilisateur pour les nouvelles classes d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd2f703e22619c8c3738b51a7a1f1464ca7e7d86b655abccd4c26258ac85810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182709"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Extension de l’interface utilisateur pour les nouvelles classes d’objets

Active Directory Domain Services et son interface utilisateur du composant logiciel enfichable MMC d’administration peuvent être personnalisés pour s’adapter aux besoins des administrateurs et des utilisateurs. Active Directory Domain Services activer le schéma pour qu’il soit modifié en créant des classes et des attributs, ou en modifiant des classes existantes. Les spécificateurs d’affichage pour les classes peuvent être modifiés pour refléter les nouveaux éléments d’interface utilisateur requis par les modifications de schéma.

Le tableau suivant répertorie les attributs qui peuvent être utilisés pour modifier la façon dont les composants logiciels enfichables d’administration affichent les objets d’une classe particulière.



| Attribut                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | L’attribut **defaultHidingValue** est un attribut d’un objet **classSchema** . cet attribut contient une valeur booléenne qui, si la valeur est TRUE, entraîne le masquage des instances de la classe d’objet dans les composants logiciels enfichables d’administration et le shell Windows. Cela signifie également qu’un élément de menu de la nouvelle classe d’objet n’apparaît pas dans le **nouveau** menu contextuel des composants logiciels enfichables d’administration, même si les propriétés appropriées de l’Assistant de création sont définies sur l’objet **displaySpecifier** de la nouvelle classe d’objets. Si cet attribut a la valeur FALSe, les instances de la classe seront visibles dans les composants logiciels enfichables d’administration et l’interpréteur de commandes. Cela entraîne également la création par un élément de menu d’une nouvelle instance d’objet à ajouter au menu **nouveau** des composants logiciels enfichables d’administration.<br/> Si aucune valeur n’est définie pour cet attribut, la valeur par défaut est TRUE. Cela signifie que, par défaut, les instances de l’objet sont masquées.<br/>                                                                |
| **showInAdvancedViewOnly** | l’attribut **showInAdvancedViewOnly** contient une valeur booléenne qui, si elle est définie sur TRUE, fait apparaître les instances de la classe d’objet dans le composant logiciel enfichable utilisateurs et ordinateurs en mode avancé uniquement et n’apparaissent pas dans le shell Windows. si cette propriété a la valeur false, les instances de la classe sont visibles en mode Normal dans le composant logiciel enfichable utilisateurs et ordinateurs et dans le shell Windows.<br/> Si aucune valeur n’est définie pour cet attribut, la valeur par défaut est TRUE.<br/> Cet attribut peut être défini sur un objet individuel pour remplacer la valeur définie sur la classe d’objet. Par exemple, la classe de **conteneur** a cet attribut défini sur true, mais le conteneur **utilisateur** a cette valeur définie sur false. Pour cette raison, le conteneur **utilisateur** apparaît dans le shell et en mode normal dans le composant logiciel enfichable utilisateurs et ordinateurs, mais les autres conteneurs qui n’ont pas de **SHOWINADVANCEDVIEWONLY** défini sur false s’affichent uniquement en mode avancé dans le composant logiciel enfichable utilisateurs et ordinateurs.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Création de spécificateurs d’affichage pour les nouvelles classes

Pour personnaliser l’interface utilisateur pour une nouvelle classe, créez un objet spécificateur d’affichage pour la nouvelle classe pour chaque paramètre régional pris en charge, puis définissez les attributs souhaités pour le spécificateur d’affichage.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Héritage des spécificateurs d’affichage pour les classes dérivées

Une nouvelle classe qui hérite d’une classe existante n’hérite pas du spécificateur d’affichage de la classe parente. Si la nouvelle classe doit utiliser une partie ou l’ensemble des propriétés du spécificateur d’affichage de la classe parente, créez un nouveau spécificateur d’affichage pour la nouvelle classe et copiez les propriétés du spécificateur d’affichage de la classe parente vers le nouveau spécificateur d’affichage de l’objet. Cela doit être fait pour tous les paramètres régionaux pour lesquels les propriétés du spécificateur d’affichage de la classe parente s’appliquent.

Certaines parties du jeu de fonctionnalités de l’interface utilisateur, telles que les éléments de menu et l’Assistant Création pour la classe utilisateur, sont implémentées en interne et ne peuvent pas être utilisées par un objet dérivé. Dans ces cas, il est préférable d’étendre une classe existante plutôt que d’utiliser une classe dérivée.

## <a name="modifying-existing-classes"></a>Modification des classes existantes

De nouveaux attributs peuvent être ajoutés à une classe existante. De nouveaux composants de l’interface utilisateur (pages de propriétés, éléments de menu et noms d’affichage des attributs) peuvent être ajoutés ou l’interface utilisateur existante doit être remplacée. Il est également possible de concevoir de nouvelles pages de propriétés qui exposent moins d’attributs d’une classe et de créer des menus contextuels avec moins d’actions. Pour plus d’informations, consultez [pages de propriétés à utiliser avec les spécificateurs d’affichage](property-pages-for-use-with-display-specifiers.md), [menus contextuels à utiliser avec les spécificateurs d’affichage](context-menus-for-use-with-display-specifiers.md), et noms d’affichage de [classe et d’attribut](class-and-attribute-display-names.md).

 

 





