---
title: Héritage de classes dans le schéma Active Directory
description: Toutes les classes d’objets dans un schéma de service d’annuaire Active Directory sont dérivées de la classe spéciale Top.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031046"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Héritage de classes dans le schéma Active Directory

Toutes les classes d’objets dans un schéma de service d’annuaire Active Directory sont dérivées de la classe spéciale [**Top**](/windows/desktop/ADSchema/c-top). À l’exception de **Top**, toutes les classes d’objets sont des sous-classes d’une autre classe d’objets. Par exemple, le [**contact**](/windows/desktop/ADSchema/c-contact) est une sous-classe de [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson); **organizationalPerson** est une sous-classe de [**Person**](/windows/desktop/ADSchema/c-person); et **Person** est une sous-classe de **Top**. L’attribut [**subClassOf**](/windows/desktop/ADSchema/a-subclassof) d’un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) est une propriété à valeur unique qui indique la superclasse immédiate de la classe.

Certaines des valeurs d’attribut qui définissent une classe sont héritées de ses superclasses. Par conséquent, la classe [**contact**](/windows/desktop/ADSchema/c-contact) hérite des valeurs de ses superclasses, qui sont les classes [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson), [**Person**](/windows/desktop/ADSchema/c-person)et [**Top**](/windows/desktop/ADSchema/c-top) . Une classe hérite des données suivantes de ses superclasses :

-   Attributs possibles : les valeurs des attributs [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)et [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) d’un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) définissent la liste complète des attributs qui peuvent être définis sur une instance de la classe d’objet. Pour chaque classe d’objet, les valeurs de ces attributs incluent toutes les valeurs qui sont héritées de ses superclasses, ainsi que toutes les valeurs qui sont définies explicitement pour la classe d’objet elle-même. Ainsi, l’attribut [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la [**classe organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson) comprend toutes les **valeurs mustContain** qui sont héritées des classes [**Person**](/windows/desktop/ADSchema/c-person) et [**Top**](/windows/desktop/ADSchema/c-top) , ainsi que toutes les valeurs **mustContain** définies explicitement sur la classe **organizationalPerson** .
-   Parents possibles dans la hiérarchie de répertoires : les valeurs des attributs [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) et [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) d’un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) définissent la liste complète des classes d’objets qui peuvent contenir une instance de la classe d’objet. Pour chaque classe d’objet, les valeurs incluent celles héritées de ses superclasses, ainsi que celles définies explicitement pour la classe d’objet elle-même.

Sachez que la classe Object peut également avoir de nombreuses classes auxiliaires, qui sont spécifiées dans les attributs [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) et [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass) d’un objet **classSchema** . Une classe d’objet hérite des valeurs [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)et [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) de ses classes auxiliaires.

 

 