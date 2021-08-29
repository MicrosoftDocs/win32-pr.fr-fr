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
ms.openlocfilehash: 8e7c55fbc499ab3747b65ace9e869a0d5930894211d73a07ab1078eef8614694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082323"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Résolution de plusieurs composants d’agrégation prenant en charge la même interface

Il est rare que deux extensions exposent la même interface à ADSI. Dans ce cas, les règles suivantes s’appliquent :

-   Si une interface, telle que **IMyInterface**, est prise en charge par l’agrégateur (ADSI) et tous les objets d’extension, **QueryInterface** retourne toujours le **IMyInterface** pour ADSI.
-   Si une interface, telle que **IMyInterface**, n’est pas prise en charge par l’agrégateur (ADSI), mais qu’elle est prise en charge par plus d’un objet d’extension, **QueryInterface** retourne le **IMyInterface** du premier objet d’extension listé dans le Registre qui prend en charge l’interface.

N’oubliez pas que l’ordre des composants dans le registre affecte également la résolution des conflits de noms dans Automation. Pour plus d’informations, consultez [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




