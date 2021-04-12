---
title: Exemples d’applications C++ BITS
description: Les exemples d’applications Service de transfert intelligent en arrière-plan (BITS) de cette section sont écrits en C++. Elles illustrent une série de tâches qui peuvent être effectuées à l’aide des fonctionnalités BITS. Chaque application est divisée en une série d’étapes.
ms.assetid: 6163c7fd-e187-4f75-bf25-e3a515e50db5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf577509dac58a655c2cbc8b602b75bd48aa03e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031609"
---
# <a name="bits-c-application-examples"></a>Exemples d’applications C++ BITS

Les exemples d’applications Service de transfert intelligent en arrière-plan (BITS) de cette section sont écrits en C++. Elles illustrent une série de tâches qui peuvent être effectuées à l’aide des fonctionnalités BITS. Chaque application est divisée en une série d’étapes.

Le tableau suivant répertorie les exemples C++ de cette section.



| Exemple                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exemple : classes communes](common-classes.md)                                                                                                                      | Cet exemple contient les classes communes utilisées pour les exemples de cette section. Ces classes communes incluent une classe de rappel, une classe d’erreur générique et une classe d’assistance d’acquisition de ressources pour la fonction COM [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) . |
| [Exemple : spécification des informations d’identification d’authentification du serveur pour une tâche de transfert BITS](example-specifying-server-authentication-credentials-for-a-bits-transfer-job-.md) | Cet exemple obtient le schéma d’autorisation et les informations d’identification de l’utilisateur, crée une tâche de transfert BITS, définit les informations d’identification pour le travail et surveille l’état du travail.                                                                                                               |
| [Exemple : utilisation de l’encodage d’authentification SSPI avec BITS.](example-using-sspi-authentication-encoding-with-bits.md)                                                 | Cet exemple illustre l’utilisation de l’authentification SSPI (Security Support Provider Interface) et du service BITS pour obtenir les informations d’identification d’un utilisateur, encoder les informations d’identification et définir les informations d’identification encodées pour une tâche de transfert BITS.                                                                |
| [Exemple : ajout d’un jeton d’assistance à une tâche de transfert BITS](example-adding-a-helper-token-to-a-bits-transfer-job-.md)                                                 | Cet exemple crée une tâche de transfert BITS et ajoute un deuxième ensemble d’informations d’identification au travail.                                                                                                                                                                                                  |



 

 

 