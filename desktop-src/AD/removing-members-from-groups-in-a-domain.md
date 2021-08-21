---
title: Suppression de membres de groupes dans un domaine
description: Vous pouvez supprimer des utilisateurs, des groupes ou des contacts des groupes.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- regroupe Active Directory, en supprimant les membres des groupes dans un domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025157"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Suppression de membres de groupes dans un domaine

Vous pouvez supprimer des utilisateurs, des groupes ou des contacts des groupes. L’attribut de **membre** de l’objet **Group** contient tous les membres directs du groupe.

La façon la plus simple de supprimer un membre d’un groupe consiste à appeler la méthode [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) sur l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) de l’objet de groupe dont vous souhaitez supprimer des membres.

 

 