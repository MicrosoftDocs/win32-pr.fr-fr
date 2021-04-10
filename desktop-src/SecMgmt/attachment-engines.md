---
description: Un moteur d’attachement est une DLL qui gère les demandes d’analyse et de configuration spécifiques aux services.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Moteurs d’attachement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866962"
---
# <a name="attachment-engines"></a>Moteurs d’attachement

Un moteur d’attachement est une DLL qui gère les demandes d’analyse et de configuration spécifiques aux services.

L’utilisateur effectue une demande de configuration et d’analyse spécifique au service à l’aide de l’extension du composant logiciel enfichable d’attachement. Cette demande est ensuite transmise à travers les composants logiciels enfichables de configuration de sécurité du moteur de configuration de sécurité général, qui à son tour transmet le traitement propre au service au moteur d’attachement approprié. Le moteur d’attachement se connecte ensuite au service et modifie sa configuration. En d’autres termes, le moteur d’attachement fournit le traitement principal qui prend en charge l’extension de composant logiciel enfichable d’attachement.

Un moteur d’attachement doit implémenter les trois fonctions suivantes :

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), qui calcule la différence entre la configuration du service et la configuration stockée dans la base de données de sécurité. Les différences sont écrites dans la base de données de sécurité.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), qui configure le service comme spécifié dans l’interface utilisateur du composant logiciel enfichable.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), qui met à jour la configuration de base et l’analyse de la configuration pour le service dans la base de données de sécurité.

Pour simplifier l’implémentation des fonctions précédentes, le jeu d’outils de configuration de la sécurité fournit des fonctions et des structures de prise en charge que votre application peut utiliser pour interroger et définir des informations dans la base de données de sécurité. Pour plus d’informations, consultez [fonctions de rappel des pièces jointes](management-functions.md).

Lorsque vous créez une DLL du moteur de pièces jointes, vous devez l’installer, puis l’inscrire auprès du moteur de configuration de la sécurité. Pour inscrire la DLL, vous devez ajouter une clé spécifique au registre. Lorsque le moteur de configuration de sécurité démarre, il vérifie le registre et charge toutes les dll du moteur de pièces jointes inscrites. Il transmet ensuite les demandes d’analyse et de configuration spécifiques au service au moteur d’attachement approprié. Les demandes de configuration et d’analyse standard, celles qui ne sont pas spécifiques au service, sont gérées par le moteur de configuration de la sécurité.

 

 



