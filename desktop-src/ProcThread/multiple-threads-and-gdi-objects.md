---
description: Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Threads multiples et objets GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524217"
---
# <a name="multiple-threads-and-gdi-objects"></a>Threads multiples et objets GDI

Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé. Cela crée un danger potentiel pour les processus qui ont plusieurs threads partageant ces objets. Par exemple, si un thread supprime un objet GDI alors qu’un autre thread l’utilise, les résultats sont imprévisibles. Ce danger peut être évité simplement en ne partageant pas d’objets GDI. Si le partage est inévitable (ou souhaitable), l’application doit fournir ses propres mécanismes pour synchroniser l’accès. Pour plus d’informations sur la synchronisation de l’accès, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).

 

 



