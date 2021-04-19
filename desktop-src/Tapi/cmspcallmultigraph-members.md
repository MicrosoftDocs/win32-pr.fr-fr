---
description: Membres CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membres CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533911"
---
# <a name="cmspcallmultigraph-members"></a>Membres CMSPCallMultiGraph

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

Les blocs d’attente stockent les informations relatives à l’attente inscrite dans le pool de threads. Il comprend les handles d’attente retournés par l’appel [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) et un pointeur vers la structure de contexte. Chaque bloc dans le tableau est destiné à un graphique dans l’un des objets de flux. Le décalage d’un bloc dans ce tableau est le même que celui du flux qui possède le graphique.

 

 
