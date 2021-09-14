---
title: Passage à l’État chargé
description: Passage à l’État chargé
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855538"
---
# <a name="entering-the-loaded-state"></a>Passage à l’État chargé

Lorsqu’un objet passe à l’État chargé, les structures en mémoire représentant l’objet sont créées afin que les opérations puissent être appelées dessus. Le gestionnaire de l’objet ou le serveur in-process est chargé. Ce processus, appelé *instanciation*, se produit lorsqu’un objet est chargé à partir d’un stockage persistant (transition de l’état passif à l’État chargé) ou lorsqu’un objet est créé pour la première fois.

En interne, l’instanciation est un processus en deux phases. Un objet de la classe appropriée est créé, après quoi une méthode sur cet objet est appelée pour effectuer l’initialisation et autoriser l’accès aux données de l’objet. La méthode d’initialisation est définie dans l’une des interfaces prises en charge par l’objet. La méthode d’initialisation particulière appelée dépend du contexte dans lequel l’objet est instancié et de l’emplacement des données d’initialisation.

 

 




