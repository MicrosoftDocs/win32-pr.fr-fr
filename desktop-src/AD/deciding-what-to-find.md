---
title: Choix des éléments à rechercher
description: Avant d’effectuer une recherche dans un répertoire, réfléchissez à la manière dont votre recherche sera effectuée en fonction de votre approche. Les données et les propriétés à retourner affectent l’emplacement où vous liez pour démarrer une recherche, la profondeur de votre recherche, le filtre de requête et les performances de recherche.
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- critères de recherche Active Directory
- détermination des Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028632"
---
# <a name="deciding-what-to-find"></a>Choix des éléments à rechercher

Avant d’effectuer une recherche dans un répertoire, réfléchissez à la manière dont votre recherche sera effectuée en fonction de votre approche. Les données et les propriétés à retourner affectent l’emplacement où vous liez pour démarrer une recherche, la profondeur de votre recherche, le filtre de requête et les performances de recherche.

Par exemple, si vous souhaitez rechercher tous les objets utilisateur avec Surname Smith :



| Domaine                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Emplacement de recherche            | Un conteneur ou une unité d’organisation (UO) spécifique au sein d’un domaine, un domaine spécifique, une arborescence de domaine spécifique ou l’ensemble de la forêt. Si vous recherchez des objets dans un conteneur ou un domaine spécifique, la requête de recherche est plus performante en liant directement ce conteneur ou ce domaine au lieu d’effectuer une recherche de sous-arborescence sur une arborescence de domaine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Type de recherche             | Si vous vérifiez l’existence de ou récupérez les propriétés d’un objet particulier qui a un nom unique (DN) que vous connaissez déjà, vous devez effectuer une recherche de base, qui recherche uniquement l’objet auquel vous êtes lié.<br/> Si vous savez qu’un objet est un descendant direct d’un conteneur particulier, effectuez une liaison à ce conteneur et effectuez une recherche à un niveau (les objets **attributeSchema** et **classSchema** dans le conteneur de schéma et les objets étendus de droite dans le conteneur de droits étendus sont de bons exemples).<br/> Si vous ne connaissez pas exactement l’emplacement de l’objet, ou si vous souhaitez Rechercher l’objet auquel vous êtes lié et tous les objets enfants situés sous celui-ci dans la hiérarchie des répertoires, effectuez une recherche dans la sous-arborescence.<br/>                                                       |
| Utiliser des index dans la mesure du possible | Enfin, si vous recherchez une classe spécifique d’objet, le filtre de requête doit avoir des expressions qui évaluent les propriétés définies pour cette classe.<br/> Pour rechercher des objets de groupe, incluez l’expression (objectCategory = Group) dans le filtre. Pour rechercher des objets utilisateur, spécifiez (& (objectClass = user) (objectCategory = person)), car la classe Computer est dérivée de la classe User. par conséquent, (objectClass = user) retourne à la fois les utilisateurs et les ordinateurs, et étant donné que les objets contact et User ont un **objectCategory** , donc (objectcategory = person) retourne les utilisateurs et les contacts.<br/> Pour plus d’informations, consultez [classe d’objet et catégorie d’objet](object-class-and-object-category.md) et [attributs indexés](indexed-attributes.md).<br/> |



 

 

 





