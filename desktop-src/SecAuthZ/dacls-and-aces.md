---
description: si un objet Windows n’a pas de liste de contrôle d’accès discrétionnaire (DACL, discretionary access control list), le système autorise tout le monde à y accéder entièrement.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACL et ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096073"
---
# <a name="dacls-and-aces"></a>DACL et ACE

si un objet Windows n’a pas de [*liste de contrôle d’accès discrétionnaire (DACL, discretionary access control list*](/windows/desktop/SecGloss/d-gly) ), le système autorise tout le monde à y accéder entièrement. Si un objet a une liste DACL, le système autorise uniquement l’accès explicitement autorisé par les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste DACL. S’il n’existe aucune ACE dans la liste DACL, le système n’autorise l’accès à personne. De même, si une liste DACL contient des ACE qui autorisent l’accès à un ensemble limité d’utilisateurs ou de groupes, le système refuse implicitement l’accès à tous les droits d’utilisateur non inclus dans les entrées de sécurité.

Dans la plupart des cas, vous pouvez contrôler l’accès à un objet à l’aide des ACE access-allowed ; vous n’avez pas besoin de refuser explicitement l’accès à un objet. L’exception est quand un ACE autorise l’accès à un groupe et que vous souhaitez refuser l’accès à un membre du groupe. Pour ce faire, placez une entrée de contrôle d’accès refusée pour l’utilisateur dans la liste DACL en avance de l’ACE access-allowed pour le groupe. Notez que l' [ordre des ACE](order-of-aces-in-a-dacl.md) est important, car le système lit les entrées de commande dans l’ordre jusqu’à ce que l’accès soit accordé ou refusé. L’ACE accès refusé de l’utilisateur doit apparaître en premier ; dans le cas contraire, lorsque le système lit l’entrée de contrôle d’accès autorisée du groupe, il accorde l’accès à l’utilisateur restreint.

L’illustration suivante montre une liste DACL qui refuse l’accès à un utilisateur et accorde l’accès à deux groupes. Les membres du groupe A obtiennent des droits d’accès en lecture, en écriture et en exécution en cumulant les droits accordés au groupe A et les droits accordés à tout le monde. L’exception est Andrew, qui se voit refuser l’accès à l’entrée de contrôle d’accès refusé en dépit du fait qu’il soit membre du groupe tout le monde.

![DACL qui accorde des droits d’accès différents en fonction de l’appartenance à un groupe](images/accctrl1.png)

 

 
