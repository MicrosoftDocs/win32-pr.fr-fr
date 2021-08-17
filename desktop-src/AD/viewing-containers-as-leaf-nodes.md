---
title: Affichage des conteneurs en tant que nœuds terminaux
description: Tout objet dans Active Directory Domain Services peut être un conteneur d’autres objets.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Affichage des conteneurs en tant que nœuds terminaux
- conteneurs Active Directory, afficher en tant que nœuds terminaux
- feuille Active Directory, affichage des conteneurs en tant que nœuds terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33713f70e1b84ded536a928f8489f4fd41461bd4e37de46a84036bc6370327db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182253"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Affichage des conteneurs en tant que nœuds terminaux

Tout objet dans Active Directory Domain Services peut être un conteneur d’autres objets. Cela peut encombrer l’interface utilisateur. il est donc possible de déclarer qu’un objet d’une classe spécifique ne doit être affiché qu’en tant que feuille dans l’interface utilisateur. L’attribut **treatAsLeaf** est un attribut spécificateur d’affichage à valeur unique qui détermine si les objets de cette classe doivent être affichés uniquement en tant qu’objets feuille. Cet attribut est une valeur booléenne qui, si la **valeur est true**, indique que les objets de la classe doivent être affichés uniquement en tant qu’éléments feuille. Si la **valeur est false**, indique que les objets de la classe peuvent être affichés sous la forme d’un conteneur ou d’une feuille. Comme tous les attributs de spécificateur d’affichage, l’attribut **treatAsLeaf** est défini par paramètres régionaux. cet attribut peut donc être localisé en fonction des besoins. Par exemple, l’attribut **treatAsLeaf** **du spécificateur d’affichage de paramètres** régionaux anglais (0409) est défini sur **true** par défaut. Ainsi, l’interface utilisateur affiche tous les objets **utilisateur** en tant qu’objets feuille.

**Pour définir la valeur de l’attribut **treatAsLeaf****

1.  Établissez une liaison avec l’attribut d’affichage souhaité dans les paramètres régionaux souhaités. Pour plus d’informations et pour obtenir un exemple de code, consultez [conteneur DisplaySpecifiers](displayspecifiers-container.md).
2.  Utilisez la [**méthode IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) pour affecter la valeur **true** ou **false** à l’attribut **treatAsLeaf** .
3.  Pour valider les modifications apportées à l’annuaire, appelez la méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .

 

 