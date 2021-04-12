---
description: Certains objets ne prennent en charge qu’un seul handle à la fois.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitations des handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210231"
---
# <a name="handle-limitations"></a>Limitations des handles

Certains objets ne prennent en charge qu’un seul handle à la fois. Le système fournit le descripteur lorsqu’une application crée l’objet et invalide le descripteur lorsque l’application détruit l’objet. Les autres objets prennent en charge plusieurs descripteurs sur un seul objet. Le système d’exploitation supprime automatiquement l’objet de la mémoire après la fermeture du dernier handle de l’objet.

Le nombre total de handles ouverts dans le système est limité uniquement par la quantité de mémoire disponible. Certains types d’objets prennent en charge un nombre limité de handles par session ou par processus.

 

 



