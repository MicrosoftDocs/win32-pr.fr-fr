---
description: Dans un contrôle d’accès, le système compare les informations de sécurité dans le jeton d’accès threads aux informations de sécurité contenues dans le descripteur de sécurité des objets.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interaction entre les threads et les objets sécurisables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670813"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interaction entre les threads et les objets sécurisables

Quand un thread tente d’utiliser un [objet sécurisable](securable-objects.md), le système effectue une vérification d’accès avant d’autoriser le thread à continuer. Dans un contrôle d’accès, le système compare les informations de sécurité dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du thread aux informations de sécurité dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet.

-   Le jeton d’accès contient des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui identifient l’utilisateur associé au thread.
-   Le descripteur de sécurité identifie le propriétaire de l’objet et contient une liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ). La liste DACL contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE), chacune spécifiant les droits d’accès accordés ou refusés à un utilisateur ou à un groupe spécifique.

Le système vérifie la liste DACL de l’objet, en recherchant les entrées de contrôle d’accès qui s’appliquent aux SID d’utilisateur et de groupe à partir du jeton d’accès du thread. Le système vérifie chaque ACE jusqu’à ce que l’accès soit accordé ou refusé, ou jusqu’à ce qu’il n’y ait plus de ACE à vérifier. En théorie, une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) peut avoir plusieurs entrées de contrôle d’accès (ACE) qui s’appliquent aux SID du jeton. Et, si cela se produit, les droits d’accès accordés par chaque ACE s’accumulent. Par exemple, si une entrée de contrôle d’accès accorde l’accès en lecture à un groupe et qu’une autre entrée de contrôle d’accès accorde l’accès en écriture à un utilisateur membre du groupe, l’utilisateur peut avoir un accès en lecture et en écriture à l’objet.

L’illustration suivante montre la relation entre ces blocs d’informations de sécurité :

![relations entre les processus, les ACE et les DACL](images/cssec-02.png)

 

 
