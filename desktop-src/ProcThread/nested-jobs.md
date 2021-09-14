---
description: Une application peut utiliser des tâches imbriquées pour gérer des sous-ensembles de processus. Les travaux imbriqués activent également une application qui utilise des travaux pour héberger d’autres applications qui utilisent également des travaux.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Tâches imbriquées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324811"
---
# <a name="nested-jobs"></a>Tâches imbriquées

Une application peut utiliser des tâches imbriquées pour gérer des sous-ensembles de processus. Les travaux imbriqués activent également une application qui utilise des travaux pour héberger d’autres applications qui utilisent également des travaux.

**Windows 7, Windows server 2008 R2, Windows XP avec SP3, Windows server 2008, Windows Vista et Windows Server 2003 :** Un processus ne peut être associé qu’à un seul travail. des tâches imbriquées ont été introduites dans Windows 8 et Windows Server 2012.

Cette rubrique fournit une vue d’ensemble de l’imbrication et du comportement des tâches imbriquées :

-   [Hiérarchies de tâches imbriquées](#nested-job-hierarchies)
-   [Création d’une hiérarchie de travaux imbriqués](#creating-a-nested-job-hierarchy)
-   [Limites du travail et notifications pour les travaux imbriqués](#job-limits-and-notifications-for-nested-jobs)
-   [Comptabilisation des ressources pour les travaux imbriqués](#resource-accounting-for-nested-jobs)
-   [Fin des tâches imbriquées](#termination-of-nested-jobs)

Pour obtenir des informations générales sur les travaux et les objets de travail, consultez [objets de traitement](job-objects.md).

## <a name="nested-job-hierarchies"></a>Hiérarchies de tâches imbriquées

Les travaux imbriqués ont une relation parent-enfant dans laquelle chaque travail enfant contient un sous-ensemble des processus dans son travail parent. Si un processus qui est déjà dans un travail est ajouté à un autre travail, les travaux sont imbriqués par défaut si le système peut former une hiérarchie de travaux valide et que ni le travail ne définit des limites d’interface utilisateur ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) avec **JobObjectBasicUIRestrictions**).

La figure 1 montre une hiérarchie de travaux qui contient une arborescence de processus étiquetés P0 à P7. Le travail 1 est le *travail parent* du travail 2 et du travail 4, et il s’agit d’un *ancêtre* du travail 3. Le travail 2 est le *parent immédiat* du travail 3 ; Le travail 3 est l' *enfant immédiat* du travail 2. Les travaux 1, 2 et 3 forment une *chaîne de travail* dans laquelle les travaux 1 et 2 sont la *chaîne de travail parent* du travail 3. La tâche de fin dans une chaîne de travaux est le *travail immédiat* des processus de cette tâche. Dans la figure 1, le travail 3 est le travail immédiat des processus P2, P3 et P4.

![Figure 1. hiérarchie de travaux imbriquée qui contient une arborescence de processus](images/nested-jobs-a.png)

Les tâches imbriquées peuvent également être utilisées pour gérer des groupes de processus homologues. Dans la hiérarchie des travaux illustrée à la figure 2, le travail 1 est le travail parent du travail 2. Notez qu’une hiérarchie de travaux ne peut contenir qu’une partie d’une arborescence de processus. Dans la figure 2, P0 n’est pas dans la hiérarchie, mais ses processus enfants P1 à P5 sont.

![Figure 2. une hiérarchie de travaux imbriquée qui contient des processus homologues](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Création d’une hiérarchie de travaux imbriqués

Les processus d’une hiérarchie de travaux sont soit explicitement associés à un objet de traitement à l’aide de la fonction [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) , soit implicitement associé pendant la création du processus, comme pour les travaux autonomes. L’ordre dans lequel les travaux sont créés et les processus attribués détermine si une hiérarchie peut être créée.

Pour créer une hiérarchie de travaux à l’aide de l’Association explicite, tous les objets de tâche doivent être créés à l’aide de [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta), puis [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) doit être appelé plusieurs fois pour chaque processus afin d’associer le processus à chaque travail auquel il doit appartenir. Pour vous assurer que la hiérarchie des travaux est valide, attribuez tout d’abord tous les processus à la tâche à la racine de la hiérarchie, puis affectez un sous-ensemble de processus à l’objet de tâche enfant immédiat, et ainsi de suite. Si des processus sont affectés à des travaux dans cet ordre, un travail enfant aura toujours un sous-ensemble de processus dans son travail parent lors de la création de la hiérarchie, ce qui est nécessaire pour l’imbrication. Si des processus sont affectés à des travaux dans un ordre aléatoire, à un moment donné, un travail enfant aura des processus qui ne se trouvent pas dans son travail parent. Cela n’est pas autorisé par l’imbrication et entraîne l’échec de **AssignProcessToJobObject** .

Lorsque des processus sont implicitement associés à un travail lors de la création du processus, un processus enfant est associé à chaque travail dans la chaîne de travail de son processus parent. Si l’objet de travail immédiat autorise la dissociation, le processus enfant s’interrompt de l’objet de traitement immédiat et de chaque travail dans la chaîne de travail parente, en se déplaçant vers le haut de la hiérarchie jusqu’à ce qu’il atteigne un travail qui n’autorise pas la dissociation. Si l’objet de traitement immédiat n’autorise pas la dissociation, le processus enfant n’est pas supprimé même si les travaux dans sa chaîne de travail parent l’autorisent.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Limites du travail et notifications pour les travaux imbriqués

Pour certaines limites de ressources, la limite définie pour les travaux dans une chaîne de travail parente détermine la *limite effective* appliquée pour un travail enfant. La limite effective du travail enfant peut être plus restrictive que la limite de son parent, mais il ne peut pas être moins restrictif. Par exemple, si la classe de priorité d’un travail enfant est supérieure à la classe de \_ \_ priorité normale et que la classe \_ de priorité de sa tâche parente est la classe de priorité normale \_ \_ , la limite effective des processus dans le travail enfant est la \_ classe de priorité normale \_ . Toutefois, si la classe de priorité du travail enfant est inférieure à la \_ \_ classe de priorité normale \_ , la limite effective des processus dans le travail enfant est inférieure à la \_ classe de priorité normale \_ \_ . Les limites effectives sont appliquées pour la classe de priorité, l’affinité, les frais de validation, la limite de durée d’exécution par processus, la limite de classe de planification et la plage de travail minimale et maximale. Pour plus d’informations sur les limites de ressources spécifiques, consultez [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Lorsque certains événements se produisent, tels que la création d’un nouveau processus ou la violation de limite des ressources, un message est envoyé au port de terminaison d’e/s associé à un travail. Un travail peut également s’inscrire pour recevoir des notifications lorsque certaines limites sont dépassées. Pour un travail non imbriqué, le message est envoyé au port de terminaison d’e/s associé au travail. Pour un travail imbriqué, le message est envoyé à chaque port de terminaison d’e/s associé à n’importe quel travail dans la chaîne de travail parent du travail qui a déclenché le message. Un travail enfant n’a pas besoin d’un port de terminaison d’e/s associé pour les messages qu’il déclenche à envoyer aux ports de terminaison d’e/s des tâches parentes plus haut dans la chaîne de travaux. Pour plus d’informations sur les messages spécifiques, consultez [**JOBOBJECT \_ Associate \_ Complete \_ port**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Comptabilisation des ressources pour les travaux imbriqués

Les informations de gestion des ressources pour un travail imbriqué décrivent l’utilisation de chaque processus associé à ce travail, y compris les processus des tâches enfants. Chaque travail d’une chaîne de travail représente par conséquent les ressources agrégées utilisées par ses propres processus et les processus de chaque travail enfant situé au-dessous de lui dans la chaîne de travaux.

## <a name="termination-of-nested-jobs"></a>Fin des tâches imbriquées

Lorsqu’un travail dans une hiérarchie de travaux est terminé, le système arrête les processus de ce travail et de tous ses travaux enfants, en commençant par le travail enfant en bas de la hiérarchie. Les ressources en suspens utilisées par chaque processus terminé sont facturées au travail parent.

Le descripteur de travail doit avoir le \_ \_ droit d’accès arrêter l’objet de travail, comme pour les travaux autonomes.

 

 
