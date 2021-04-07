---
title: Suppression de membres de groupes dans un domaine
description: Vous pouvez supprimer des utilisateurs, des groupes ou des contacts des groupes.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- regroupe Active Directory, en supprimant les membres des groupes dans un domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724445"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Suppression de membres de groupes dans un domaine

Vous pouvez supprimer des utilisateurs, des groupes ou des contacts des groupes. L’attribut de **membre** de l’objet **Group** contient tous les membres directs du groupe.

La façon la plus simple de supprimer un membre d’un groupe consiste à appeler la méthode [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) sur l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) de l’objet de groupe dont vous souhaitez supprimer des membres.

 

 