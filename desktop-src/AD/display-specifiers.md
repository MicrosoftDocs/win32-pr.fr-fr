---
title: Spécificateurs d’affichage
description: Dans Active Directory Domain Services, une classe d’objet, ou classe, définit un type d’objet qui peut être créé dans Active Directory Domain Services.
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940831"
---
# <a name="display-specifiers"></a>Spécificateurs d’affichage

Dans Active Directory Domain Services, une classe d’objet, ou classe, définit un type d’objet qui peut être créé dans Active Directory Domain Services. La définition de chaque classe d’objet est stockée sous la forme d’un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) dans le [schéma de Active Directory](active-directory-schema.md). En plus de la définition de **classSchema** , chaque classe d’objet peut avoir un ou plusieurs spécificateurs d’affichage qui spécifient les données de l’interface utilisateur pour les objets de cette classe.

Un spécificateur d’affichage est un objet de la classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) . Les attributs d’un objet **displaySpecifier** spécifient des données d’interface utilisateur localisées qui décrivent les différents éléments d’interface utilisateur pour une classe d’objet particulière. Les spécificateurs d’affichage stockent des données pour les feuilles de propriétés, les menus contextuels, les icônes, les assistants de création et les noms de classe localisée et d’attribut. Pour les pages de propriétés et les menus contextuels, le shell Windows et les composants logiciels enfichables d’Active Directory utilisent ces données pour former des interfaces utilisateur différentes pour les administrateurs et les utilisateurs finaux : un ensemble de pages de propriétés et/ou de menus contextuels peut être associé à des applications administratives, tandis qu’un autre ensemble d’éléments peut être associé à des applications utilisateur final.

Les objets [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) sont stockés dans des conteneurs spécifiques aux paramètres régionaux dans le conteneur DisplaySpecifiers du conteneur Configuration, qui est répliqué sur chaque contrôleur de domaine de la forêt d’entreprise. Le conteneur DisplaySpecifiers contient des sous-conteneurs qui correspondent aux différents paramètres régionaux pris en charge par l’installation de l’entreprise. Ces sous-conteneurs sont nommés à l’aide d’identificateurs de langue. Par exemple, le nom du conteneur de paramètres régionaux pour US-English est 409, qui correspond à l’identificateur de langue hexadécimal, 0x0409. Par conséquent, une classe d’objet peut avoir plusieurs spécificateurs d’affichage : un dans chaque sous-conteneur de paramètres régionaux. Pour plus d’informations et pour obtenir la liste des identificateurs de langage possibles, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langue. Pour plus d’informations sur les paramètres régionaux, consultez [paramètres régionaux et langues](/windows/desktop/Intl/locales-and-languages).

Le nom d’un objet [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) est formé en ajoutant la chaîne « -Display » au [**lDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) de la classe d’objet. Par exemple, le nom d’un objet **displaySpecifier** pour la classe [**User**](/windows/desktop/ADSchema/c-user) est « user-Display ».

Vous pouvez ajouter, supprimer ou modifier les propriétés des objets [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) d’une classe pour spécifier les éléments d’interface utilisateur (nom de la classe, noms des attributs, feuilles de propriétés, menus contextuels, icône, etc.) qui s’affichent pour chaque instance d’un objet de cette classe.

Pour plus d’informations sur les spécificateurs d’affichage, consultez [conteneur DisplaySpecifiers](displayspecifiers-container.md).

 

 