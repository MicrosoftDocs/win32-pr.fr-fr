---
description: Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Threads multiples et objets GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a17c7edcf32341eb9b1eaff3546fbe7be219b5f924a85d4a1db1d584a0a5922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032329"
---
# <a name="multiple-threads-and-gdi-objects"></a>Threads multiples et objets GDI

Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé. Cela crée un danger potentiel pour les processus qui ont plusieurs threads partageant ces objets. Par exemple, si un thread supprime un objet GDI alors qu’un autre thread l’utilise, les résultats sont imprévisibles. Ce danger peut être évité simplement en ne partageant pas d’objets GDI. Si le partage est inévitable (ou souhaitable), l’application doit fournir ses propres mécanismes pour synchroniser l’accès. Pour plus d’informations sur la synchronisation de l’accès, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).

 

 



