---
description: Lorsqu’une erreur se produit, l’administrateur système ou le représentant du support technique doit déterminer la cause de l’erreur, tenter de récupérer les données perdues et empêcher l’erreur de se reproduire.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: À propos de la journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9f30e4f8a44594b95215d748ac5cafda6b0633eefa668d0d864362c8f3c5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814256"
---
# <a name="about-event-logging"></a>À propos de la journalisation des événements

Lorsqu’une erreur se produit, l’administrateur système ou le représentant du support technique doit déterminer la cause de l’erreur, tenter de récupérer les données perdues et empêcher l’erreur de se reproduire. Il est utile si les applications, le système d’exploitation et d’autres services système enregistrent des événements importants, tels que des conditions de mémoire insuffisante ou des tentatives excessives d’accès à un disque. L’administrateur système peut ensuite utiliser le journal des événements pour déterminer les conditions à l’origine de l’erreur et identifier le contexte dans lequel elle s’est produite. En affichant régulièrement le journal des événements, l’administrateur système peut être en mesure d’identifier les problèmes (tels qu’un disque dur défaillant) avant qu’ils ne provoquent des dommages.

> [!Note]  
> l’API de journalisation des événements a été conçue pour les applications qui s’exécutent sur le système d’exploitation Windows Server 2003, Windows XP ou Windows 2000. dans Windows Vista, l’infrastructure de journalisation des événements a été repensée. les Applications conçues pour s’exécuter sur les systèmes d’exploitation Windows Vista ou versions ultérieures doivent désormais utiliser [Windows journal](/windows/desktop/WES/windows-event-log) des événements pour consigner les événements.

 
Cette section décrit l’interface de programmation pour l’écriture et l’utilisation d’événements à l’aide de la journalisation des événements.

-   [Types d’événements](event-types.md)
-   [Instructions de journalisation](logging-guidelines.md)
-   [Éléments de journalisation des événements](event-logging-elements.md)
-   [Opérations de journalisation des événements](event-logging-operations.md)
-   [Modèle de journalisation des événements](event-logging-model.md)
-   [Sécurité de la journalisation des événements](event-logging-security.md)

> [!Note]  
> les Applications qui publient des événements d’une taille supérieure à 64 kilo-octets sur un ordinateur Windows Server 2003, Windows XP ou Windows 2000 ne sont pas en mesure de publier des événements sur un ordinateur Windows Vista ou version ultérieure.
