---
description: Les exigences de sécurité de niveau C2 spécifient que les administrateurs système doivent être en mesure d’auditer les événements liés à la sécurité et que l’accès à ces données d’audit doit être limité aux administrateurs autorisés.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Génération de l’audit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013713"
---
# <a name="audit-generation"></a>Génération de l’audit

Les exigences de sécurité de niveau C2 spécifient que les administrateurs système doivent être en mesure d’auditer les événements liés à la sécurité et que l’accès à ces données d’audit doit être limité aux administrateurs autorisés. l’API Windows fournit des fonctions permettant à un administrateur de surveiller les événements liés à la sécurité.

Le descripteur de sécurité d’un objet sécurisable peut avoir une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Une liste SACL contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) qui spécifient les types de tentatives d’accès qui génèrent des rapports d’audit. Chaque ACE identifie un tiers de confiance, un ensemble de droits d’accès et un ensemble d’indicateurs qui indiquent si le système génère des messages d’audit pour les échecs de tentative d’accès, les tentatives d’accès réussies ou les deux.

Le système écrit des messages d’audit dans le journal des événements de sécurité. Pour plus d’informations sur l’accès aux enregistrements dans un journal des événements de sécurité, consultez [journalisation des événements](/windows/desktop/EventLog/event-logging).

pour lire ou écrire la liste SACL d’un objet, un thread doit tout d’abord activer le \_ privilège SE nom de sécurité \_ . Pour plus d’informations, consultez [droit d’accès SACL](sacl-access-right.md).

l’API Windows fournit également une prise en charge pour les applications serveur afin de générer des messages d’audit lorsqu’un client essaie d’accéder à un objet privé. Pour plus d’informations, consultez [audit de l’accès aux objets privés](auditing-access-to-private-objects.md).

 

 
