---
description: Certains objets ne prennent en charge qu’un seul handle à la fois.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitations des handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f194ed8464d2731c15e9b88ae62549f9fa090928c14cf7dc66e139944863b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764407"
---
# <a name="handle-limitations"></a>Limitations des handles

Certains objets ne prennent en charge qu’un seul handle à la fois. Le système fournit le descripteur lorsqu’une application crée l’objet et invalide le descripteur lorsque l’application détruit l’objet. Les autres objets prennent en charge plusieurs descripteurs sur un seul objet. Le système d’exploitation supprime automatiquement l’objet de la mémoire après la fermeture du dernier handle de l’objet.

Le nombre total de handles ouverts dans le système est limité uniquement par la quantité de mémoire disponible. Certains types d’objets prennent en charge un nombre limité de handles par session ou par processus.

 

 



