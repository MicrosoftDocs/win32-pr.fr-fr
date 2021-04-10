---
title: Indicateurs de transaction
description: Un objet peut être ouvert en mode direct ou traité.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196943"
---
# <a name="transaction-flags"></a>Indicateurs de transaction

Un objet peut être ouvert en mode direct ou traité. Lorsqu’un objet est ouvert en mode direct, les modifications sont apportées immédiatement et de façon permanente. Lorsqu’un objet est ouvert en mode traité, les modifications sont mises en mémoire tampon afin qu’elles puissent être explicitement validées ou rétablies une fois la modification terminée. Les modifications validées sont enregistrées dans l’objet pendant que les modifications annulées sont ignorées. Le mode direct est le mode d’accès par défaut.

Le mode transactionnel n’est pas requis sur un objet de stockage parent pour pouvoir être utilisé sur un élément imbriqué. Toutefois, une transaction pour un élément imbriqué est imbriquée dans la transaction pour son objet de stockage parent. Par conséquent, les modifications apportées à un objet enfant ne peuvent pas être validées tant que celles-ci n’ont pas été validées, et elles restent non validées jusqu’à ce que l’objet de stockage racine (le parent de niveau supérieur) soit effectivement écrit sur le disque. En d’autres termes, les modifications se déplacent vers l’extérieur : les objets internes publient les modifications apportées aux transactions de leurs conteneurs immédiats.

 

 




