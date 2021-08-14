---
title: Instructions relatives à la liaison au schéma
description: Il existe deux façons de lier le Active Directory schéma à la liaison directe au conteneur de schéma ou à un objet classSchema ou attributeSchema dans le conteneur de schéma.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Instructions relatives à la liaison à la publicité de schéma
- Schéma AD, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188683"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Instructions relatives à la liaison au schéma

Il existe deux façons de lier le schéma de Active Directory :

-   Liez directement au conteneur de schéma ou à un objet **classSchema** ou **attributeSchema** dans le conteneur de schéma. Les objets **classSchema** ou **attributeSchema** contiennent des définitions complètes et formelles de chaque classe et attribut qui peut exister dans une forêt domaine Active Directory. Pour plus d’informations, consultez [lecture des objets AttributeSchema et classSchema](reading-attributeschema-and-classschema-objects.md).
-   Effectuer une liaison au schéma abstrait ou à une entrée de classe ou d’attribut dans le schéma abstrait. Le schéma abstrait contient uniquement un sous-ensemble des données relatives à chaque classe et attribut, mais les données sont dans un format facile à récupérer et à utiliser. Pour plus d’informations, consultez [le schéma abstrait](the-abstract-schema.md) et [la lecture du schéma abstrait](reading-the-abstract-schema.md).

Pour modifier ou étendre le schéma, établissez une liaison directe avec le conteneur de schéma. Pour lire les définitions de classe et d’attribut, il est généralement plus facile de lire à partir du schéma abstrait.

Il est plus facile de lire le schéma abstrait pour les raisons suivantes :

-   ADSI fournit des techniques de liaison spéciales et un ensemble d’interfaces permettant de lire le schéma abstrait.
-   Les interfaces ADSI qui fonctionnent avec le schéma abstrait retournent des données dans un format approprié pour une utilisation dans d’autres interfaces ADSI. Par exemple, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) et [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) utilisent généralement des chaînes **lDAPDisplayName** pour signaler des noms d’attribut et de classe, même si ces données sont stockées dans l’annuaire sous la forme d’identificateurs d’objets (OID). Le format **lDAPDisplayName** est pratique, car d’autres interfaces ADSI l’utilisent pour faire référence à des classes et des attributs dans des filtres de recherche et ailleurs.
-   L’entrée de schéma abstrait pour une classe d’objet contient les données collectées à partir de plusieurs objets **classSchema** . Par exemple, les parents possibles, les attributs obligatoires et les attributs facultatifs d’une classe d’objet sont l’Union de ces attributs à partir des superclasses et des classes auxiliaires de la classe. Si vous lisez à partir du conteneur de schéma réel, vous devez collecter des données à partir des différents objets **classSchema** desquels la classe a été dérivée. Si vous lisez à partir du schéma abstrait, les données se trouvent à un seul endroit.

Vous devez effectuer une liaison directe avec le conteneur de schéma plutôt que d’utiliser le schéma abstrait dans les cas suivants :

-   Pour récupérer des attributs spécifiques qui ne sont pas exposés dans le schéma abstrait. Par exemple, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** et d’autres attributs ne sont pas exposés dans le schéma abstrait.
-   Pour interroger les objets **attributeSchema** et **classSchema** . Pour rechercher des classes ou des attributs qui correspondent à un filtre spécifié, effectuez une liaison au conteneur de schéma et effectuez une recherche à un niveau.
-   Pour ajouter ou modifier des attributs ou des classes. Le schéma abstrait est en lecture seule ; vous ne pouvez pas l’utiliser pour modifier ou étendre le schéma. N’oubliez pas que les modifications doivent être apportées au contrôleur de domaine qui est le contrôleur de schéma. Pour plus d’informations, consultez [Configuration requise pour l’installation d’une extension de schéma](prerequisites-for-installing-a-schema-extension.md).

 

 