---
title: Conteneurs et feuilles
description: Active Directory Domain Services contenir une hiérarchie d’objets dans laquelle chaque instance d’objet, à l’exception de la racine de la hiérarchie de répertoires, est contenue dans un autre objet.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- conteneurs et feuilles Active Directory
- Active Directory feuille
- Active Directory de conteneur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462910"
---
# <a name="containers-and-leaves"></a>Conteneurs et feuilles

Active Directory Domain Services contenir une hiérarchie d’objets dans laquelle chaque instance d’objet, à l’exception de la racine de la hiérarchie de répertoires, est contenue dans un autre objet. La structure de cette hiérarchie est plus flexible qu’un système de fichiers de répertoires et de fichiers. Au lieu de cela, les règles, dans le [schéma Active Directory](active-directory-schema.md), déterminent les classes d’objets qui peuvent contenir des instances d’autres classes d’objets. Par exemple, la définition de schéma par défaut de la classe d’objet [**utilisateur**](/windows/desktop/ADSchema/c-user) comprend les classes [**d’unité d’organisation et d'**](/windows/desktop/ADSchema/c-organizationalunit) objet [**conteneur**](/windows/desktop/ADSchema/c-container) comme valeurs supérieures possibles. autrement dit, les objets parents ou les conteneurs possibles d’une instance d’objet **utilisateur** . Cela signifie qu’un objet **d’unité d’organisation** peut contenir un objet **utilisateur** , mais qu’un objet **utilisateur** ne peut pas contenir un autre objet **utilisateur** , à moins que la définition de schéma de la classe **utilisateur** ne soit modifiée.

À l’exception des objets de schéma, autrement dit, des objets [**classSchema**](/windows/desktop/ADSchema/c-classschema) ou [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) qui définissent les classes et les attributs qui peuvent exister dans une forêt de serveurs, tout objet dans Active Directory Domain Services peut être un conteneur. Plus précisément, toute classe d’objet qui apparaît dans l’attribut [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) ou [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) d’une définition de classe d’objet est potentiellement un conteneur. Pour plus d’informations sur les conteneurs d’une classe d’objet prédéfinie, consultez [Active Directory Domain Services référence](active-directory-domain-services-reference.md). Vous pouvez lier par programmation au schéma abstrait et utiliser les méthodes [**IADsClass :: obtenir la \_ relation contenant-contenu**](/windows/desktop/api/iads/nn-iads-iadsclass) ou [**IADsClass :: obtenir \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) pour obtenir les classes qu’une classe donnée peut contenir ou être contenue dans. Pour plus d’informations, consultez [lecture du schéma abstrait](reading-the-abstract-schema.md). Vous pouvez également lire l’attribut [**PossibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) d’une instance d’objet pour déterminer les classes d’objets que l’objet peut contenir. Sachez que **PossibleInferiors** est un attribut construit, ce qui signifie qu’il est calculé à partir des valeurs **possSuperiors** / **systemPossSuperiors** des autres définitions de classe et qu’il n’est pas réellement stocké dans l’annuaire.

N’oubliez pas que le schéma Active Directory définit une classe de [**conteneur**](/windows/desktop/ADSchema/c-container) . Comme nous l’avons vu précédemment, un objet ne doit pas obligatoirement être une instance de la classe de **conteneur** pour être un conteneur. Il y a également une classe [**feuille**](/windows/desktop/ADSchema/c-leaf) , bien que les sous-classes de cette classe ne soient généralement pas des conteneurs, il n’y a aucune raison pour laquelle elles ne peuvent pas l’être.

Enfin, vous pouvez définir un indicateur sur le spécificateur d’affichage associé à une classe d’objet pour indiquer que les interfaces utilisateur doivent toujours afficher les instances de la classe comme des feuilles et non des conteneurs. Cela permet d’éviter que l’interface utilisateur ne soit encombrée par un trop grand nombre de conteneurs. Pour plus d’informations, consultez [affichage des conteneurs en tant que nœuds terminaux](viewing-containers-as-leaf-nodes.md).

 

 