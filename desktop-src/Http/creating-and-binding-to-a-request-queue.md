---
title: Création et liaison à une file d’attente de demandes
description: Une file d’attente de demandes est une file d’attente de service qui contient les demandes en attente pour une application spécifique.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914279"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Création et liaison à une file d’attente de demandes

Une file d’attente de demandes est une file d’attente de service qui contient les demandes en attente pour une application spécifique. Une application crée la file d’attente de demandes indépendamment du groupe d’URL ou de la session serveur en appelant la fonction [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) et définit les propriétés de la file d’attente des demandes en appelant la fonction [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) . Ces propriétés sont les commentaires des réponses 503, la longueur maximale de la file d’attente et l’état de l’activité.

Pour que les demandes soient acheminées vers sa file d’attente de demandes, l’application lie le groupe d’URL qu’il a créé dans le cadre de la configuration de l' [exécution](run-time-configuration.md) à la file d’attente en appelant [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) avec **HttpServerBindingProperty** spécifié dans le paramètre *Property* . Les demandes entrantes des URL dans le groupe sont ensuite acheminées vers la file d’attente de demandes spécifiée.

 

 




