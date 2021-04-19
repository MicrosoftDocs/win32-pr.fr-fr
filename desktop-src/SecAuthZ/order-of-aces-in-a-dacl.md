---
description: Lorsqu’un processus tente d’accéder à un objet sécurisable, le système passe par les entrées de contrôle d’accès (ACE) de la liste de contrôle d’accès discrétionnaire (DACL) des objets jusqu’à ce qu’il trouve des ACE qui autorisent ou refusent l’accès demandé.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordre des entrées de commande dans une liste DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520618"
---
# <a name="order-of-aces-in-a-dacl"></a>Ordre des entrées de commande dans une liste DACL

Lorsqu’un [*processus*](/windows/desktop/SecGloss/p-gly) tente d’accéder à un objet sécurisable, le système passe par des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) de l’objet jusqu’à ce qu’il trouve des ACE qui autorisent ou refusent l’accès demandé. Les droits d’accès qu’un DACL permet à un utilisateur peuvent varier en fonction de l’ordre des entrées de commande dans la liste DACL. Par conséquent, le système d’exploitation Windows XP définit un ordre préféré pour les ACE dans la liste DACL d’un objet sécurisable. L’ordre par défaut fournit un Framework simple qui garantit qu’une entrée de contrôle d’accès refusée refuse réellement l’accès. Pour plus d’informations sur l’algorithme du système de vérification de l’accès, consultez [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md).

Pour Windows Server 2003 et Windows XP, l’ordre approprié des ACE est compliqué par l’introduction des ACE spécifiques aux objets et de l’héritage automatique.

Les étapes suivantes décrivent l’ordre par défaut :

1.  Toutes les entrées ACE explicites sont placées dans un groupe avant les ACE héritées.
2.  Dans le groupe d’ACE explicites, les ACE Access-denied sont placées avant les ACE access-allowed.
3.  Les ACE héritées sont placées dans l’ordre dans lequel elles sont héritées. Les ACE héritées du parent de l’objet enfant viennent en premier, puis les ACE héritées du grand-parent, et ainsi de suite sur l’arborescence des objets.
4.  Pour chaque niveau d’ACE héritées, les ACE Access-denied sont placées avant les ACE access-allowed.

Bien entendu, tous les types ACE ne sont pas requis dans une liste de contrôle d’accès.

Les fonctions telles que [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) et [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) ajoutent une entrée de contrôle d’accès à la fin d’une liste de contrôle d’accès. Il incombe à l’appelant de s’assurer que les ACE sont ajoutées dans l’ordre approprié.

 

 
