---
description: Différences entre les e/s locales et les e/s réseau sur Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Différences dans les e/s locales et réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526131"
---
# <a name="differences-in-local-and-network-io"></a>Différences dans les e/s locales et réseau

Il existe des différences notables entre les e/s locales et les e/s réseau sur Windows :

-   La prise en charge des e/s réseau dépend du redirecteur et du protocole réseau.
-   Les performances d’e/s réseau dépendent du nombre d’opérations d’e/s réseau effectuées et de la vitesse de la connexion réseau. Votre application doit être en mesure de gérer les opérations d’e/s réseau avec des serveurs qui peuvent être beaucoup plus rapides ou plus lents que votre ordinateur local, ainsi que des modifications transitoires de la capacité du réseau. Dans ce cas, votre application peut avoir besoin de plus de temps pour terminer l’opération.
-   Les fonctions que vous utilisez pour effectuer des e/s de fichier local peuvent se comporter différemment sur le réseau. Par exemple, une opération d’e/s réseau qui prend beaucoup de temps pour s’exécuter peut expirer. Dans certains cas, les descripteurs de fichiers peuvent être laissés ouverts indéfiniment. Autre exemple : les fonctions peuvent retourner des codes d’erreur que votre application doit traiter et qui sont spécifiques aux e/s réseau.

 

 



