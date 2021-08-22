---
title: Énumération des membres d’un groupe
description: en savoir plus sur l’énumération des membres d’un groupe de Azure Active Directory. Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Énumération des membres d’un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426e2fb4fdd47f5f5b277618cb0989d8d8b06b6491d505ece20139e373ebe01f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429484"
---
# <a name="enumerating-members-in-a-group"></a>Énumération des membres d’un groupe

Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé **member**. Pour les groupes avec une appartenance de petite à moyenne taille, utilisez la méthode [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) pour obtenir un pointeur vers un objet [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) qui contient la liste de tous les membres. Utilisez ensuite la [**\_ \_ NewEnum IADsMembers :: acobtiens**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) pour récupérer un objet énumérateur que vous pouvez utiliser pour énumérer les membres.

Si l’appartenance à un groupe anticipée sera de 1000 membres ou plus, utilisez pour récupérer des utilisateurs une plage à la fois. Pour plus d’informations sur l’utilisation de pour énumérer des membres, consultez [énumération des groupes qui contiennent de nombreux membres](enumerating-groups-that-contain-many-members.md).

 

 