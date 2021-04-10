---
title: Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe
description: La méthode IADsGroup. IsMember peut être utilisée pour déterminer si un objet est membre d’un groupe.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe AD
- regroupe Active Directory, en déterminant l’appartenance d’un utilisateur ou d’un groupe à un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031019"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>Détermination de l’appartenance d’un utilisateur ou d’un groupe à un groupe

La méthode [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) peut être utilisée pour déterminer si un objet est membre d’un groupe. Cette méthode retourne la **valeur true** si l’objet spécifié est un membre direct du groupe, autrement dit, si la propriété de membre du groupe contient l’objet spécifié.

Un groupe peut contenir d’autres groupes. La méthode [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) ne vérifie pas de manière récursive les membres des groupes dans sa propriété de membre, les groupes au sein de ces groupes, etc. Pour vérifier de manière récursive qu’un objet est membre d’un groupe, énumérez les groupes dans la propriété de membre, vérifiez les membres de ces groupes pour déterminer si l’objet est un membre et, si ces groupes contiennent d’autres groupes, vérifiez leurs membres, et ainsi de suite.

> [!Note]  
> Comme les groupes peuvent être imbriqués, l’appartenance à un groupe peut avoir des boucles. Tout script qui énumère plusieurs groupes doit conserver une liste interne de groupes pour terminer la récursivité si un groupe a déjà été visité.

 

 

 