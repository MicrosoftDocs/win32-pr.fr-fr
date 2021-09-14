---
title: Résolution de plusieurs composants d’agrégation prenant en charge la même interface
description: Il est rare que deux extensions exposent la même interface à ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Résolution de plusieurs composants d’agrégation prenant en charge la même interface ADSI
- résolution de plusieurs composants d’agrégation prenant en charge la même interface ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117953"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Résolution de plusieurs composants d’agrégation prenant en charge la même interface

Il est rare que deux extensions exposent la même interface à ADSI. Dans ce cas, les règles suivantes s’appliquent :

-   Si une interface, telle que **IMyInterface**, est prise en charge par l’agrégateur (ADSI) et tous les objets d’extension, **QueryInterface** retourne toujours le **IMyInterface** pour ADSI.
-   Si une interface, telle que **IMyInterface**, n’est pas prise en charge par l’agrégateur (ADSI), mais qu’elle est prise en charge par plus d’un objet d’extension, **QueryInterface** retourne le **IMyInterface** du premier objet d’extension listé dans le Registre qui prend en charge l’interface.

N’oubliez pas que l’ordre des composants dans le registre affecte également la résolution des conflits de noms dans Automation. Pour plus d’informations, consultez [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




