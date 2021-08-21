---
description: Un moteur d’attachement est une DLL qui traite les demandes d’analyse et de configuration spécifiques au service. En d’autres termes, il gère le traitement qui ne peut pas être géré par le jeu d’outils de configuration de sécurité standard.
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: Création d’un moteur de pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4705de9babaa7316d339cccadb6e7b39f44dd6f68957659b069759550e2b537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969522"
---
# <a name="creating-an-attachment-engine"></a>Création d’un moteur de pièce jointe

Un moteur d’attachement est une DLL qui traite les demandes d’analyse et de configuration spécifiques au service. En d’autres termes, il gère le traitement qui ne peut pas être géré par le jeu d’outils de configuration de sécurité standard.

Pour créer un moteur de pièce jointe, vous devez implémenter les trois fonctions suivantes :

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), qui calcule la différence entre la configuration du service et la configuration stockée dans la base de données de sécurité. Ces différences sont écrites dans la base de données de sécurité. Pour plus d’informations, consultez [implémentation de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), qui configure le service comme spécifié dans l’interface utilisateur du composant logiciel enfichable. Pour plus d’informations, consultez [implémentation de SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md).
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), qui met à jour la configuration de base et l’analyse de la configuration pour le service dans la base de données de sécurité. Pour plus d’informations, consultez [implémentation de SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md).

L’ensemble d’outils de configuration de la sécurité implémente un ensemble de fonctions de prise en charge que votre application peut appeler pour interroger et définir des informations dans la base de données de sécurité. Pour plus d’informations, consultez [fonctions de rappel des pièces jointes](management-functions.md).

Après avoir créé une DLL du moteur de pièces jointes, vous devez l’inscrire auprès du jeu d’outils de configuration de la sécurité. Ce processus est décrit dans [inscription d’un moteur de pièces jointes](registering-an-attachment-engine.md).

En plus de créer un moteur de pièces jointes, vous devez également créer une extension de composant logiciel enfichable d’attachement. L’extension de composant logiciel enfichable fournit une interface utilisateur pour les tâches spécifiques au service. Lorsque l’utilisateur spécifie une nouvelle configuration à l’aide d’une extension de composant logiciel enfichable, la demande est transmise au moteur d’attachement approprié. Le moteur se connecte ensuite au service et modifie sa configuration. Si vous n’implémentez pas d’extension de composant logiciel enfichable, les utilisateurs n’ont aucun moyen de modifier la configuration ou l’analyse du service. Pour plus d’informations sur la création d’une extension de composant logiciel enfichable d’attachement, consultez [création d’une extension de composant logiciel enfichable en pièce jointe](creating-an-attachment-snap-in-extension.md).

 

 



