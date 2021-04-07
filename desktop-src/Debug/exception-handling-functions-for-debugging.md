---
description: Quand une exception se produit dans un processus en cours de débogage, le système notifie le débogueur en lui passant l’exception. C’est ce que l’on appelle une notification de première chance. Le système suspend ensuite tous les threads du processus en cours de débogage.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Fonctions de gestion des exceptions pour le débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846933"
---
# <a name="exception-handling-functions-for-debugging"></a>Fonctions de gestion des exceptions pour le débogage

Quand une exception se produit dans un processus en cours de débogage, le système notifie le débogueur en lui passant l’exception. C’est ce que l’on appelle *une notification de première chance*. Le système suspend ensuite tous les threads du processus en cours de débogage.

Si le débogueur ne gère pas l’exception, le système tente de localiser un gestionnaire d’exceptions approprié. Si le système ne parvient pas à localiser un ordinateur approprié, le système informe à nouveau le débogueur qu’une exception s’est produite. C’est ce que l’on appelle la « *notification de dernière chance »*. Si le débogueur ne gère pas l’exception après la dernière notification de chance, le système met fin au processus en cours de débogage.

Pour plus d’informations, consultez [gestion des exceptions du débogueur](debugger-exception-handling.md).

 

 



