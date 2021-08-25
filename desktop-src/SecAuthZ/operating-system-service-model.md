---
description: Une application s’exécutant en tant qu’utilisateur standard communique avec un service exécuté en tant que système à l’aide d’un appel de procédure distante (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modèle de service du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907799"
---
# <a name="operating-system-service-model"></a>Modèle de service du système d’exploitation

Dans le modèle de service du système d’exploitation, une application qui s’exécute en tant qu’utilisateur standard communique avec un service exécuté en tant que **système** à l’aide d’un [appel de procédure distante](/windows/desktop/Rpc/rpc-start-page) (RPC).

L’application utilisateur standard est marquée dans le manifeste de l’application avec un **requestedExecutionLevel** de **asInvoker**. Pour effectuer une opération qui requiert des privilèges d’administrateur, l’application utilisateur standard envoie une demande au service.

Une utilisation pour le modèle de service du système d’exploitation consiste à gérer les applications qui peuvent avoir un impact sur le système, telles que les antivirus ou autres logiciels indésirables et logiciels espions. L’application utilisateur standard permet à l’utilisateur connecté de contrôler certains aspects du service. Le service est chargé de déterminer les opérations qu’il effectue pour une application utilisateur standard. Par exemple, un service antivirus peut permettre à un utilisateur standard de démarrer une analyse du système, mais il risque de ne pas autoriser un utilisateur standard à désactiver la vérification des virus en temps réel.

L’un des principaux avantages de l’utilisation du modèle de service du système d’exploitation est qu’aucune invite d’élévation n’est requise.

L’un des inconvénients de l’utilisation du modèle de service du système d’exploitation est qu’un service s’exécutant sur le système utilise plus de ressources qu’une tâche et qu’un service ne peut pas être arrêté par un utilisateur standard. Envisagez d’utiliser le [modèle de tâche avec élévation de privilèges](elevated-task-model.md) si cela suffit.

Pour implémenter le modèle de service du système d’exploitation, créez une application cliente utilisateur standard et un service de système d’exploitation. Installez le service dans le système d’exploitation pendant l’heure d’installation du produit.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications nécessitant des privilèges d’administrateur](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modèle de Broker administrateur](administrator-broker-model.md)
</dt> <dt>

[Modèle d’objet COM administrateur](administrator-com-object-model.md)
</dt> <dt>

[Modèle de tâche avec élévation de privilèges](elevated-task-model.md)
</dt> </dl>

 

 
