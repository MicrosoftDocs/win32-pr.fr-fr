---
description: Le gestionnaire de contrôle des services (SCM) contrôle un service en envoyant des événements de contrôle de service à la routine du gestionnaire de contrôle des services.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Services multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003727"
---
# <a name="multithreaded-services"></a>Services multithread

Le gestionnaire de contrôle des services (SCM) contrôle un service en envoyant des événements de contrôle de service à la routine du gestionnaire de contrôle du service. Le service doit répondre en temps utile aux événements de contrôle afin que le SCM puisse effectuer le suivi de l’état du service. En outre, l’état du service doit correspondre à la description de l’état que le SCM reçoit.

En raison de ce mécanisme de communication entre un service et le SCM, vous devez être prudent lorsque vous utilisez plusieurs threads dans un service. Lorsqu’un service est invité à s’arrêter par le SCM, il doit attendre la fin de tous les threads avant de signaler au SCM que le service est arrêté. Dans le cas contraire, le SCM peut être perturbé par l’état du service et risque de ne pas s’arrêter correctement.

Le SCM doit être informé que le service répond à l’événement de contrôle d’arrêt et que la progression de l’arrêt du service est en cours. Le SCM part du principe que le service est en cours de progression si le service répond (via [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) au cours de la période (indicateur d’attente) spécifiée dans l’appel précédent à **SetServiceStatus**, et que le point de contrôle est mis à jour pour être plus grand que le point de contrôle spécifié dans l’appel précédent à **SetServiceStatus**.

Si le service signale au SCM que le service s’est arrêté avant la sortie de tous les threads, il est possible que le SCM interprète cela comme une contradiction. Cela peut aboutir à un État dans lequel le service ne peut pas être arrêté ou redémarré.

 

 



