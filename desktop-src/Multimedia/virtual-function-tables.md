---
title: Tables de fonctions virtuelles
description: Tables de fonctions virtuelles
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135496"
---
# <a name="virtual-function-tables"></a>Tables de fonctions virtuelles

Une table de fonctions virtuelles est un tableau de pointeurs vers les méthodes prises en charge par un objet. Si vous utilisez C, un objet apparaît sous la forme d’une structure dont le premier membre est un pointeur vers la table de fonctions virtuelles (**lpVtbl**); autrement dit, le premier membre pointe vers un tableau contenant des pointeurs de fonction. Les méthodes prennent toutes un pointeur vers la table de fonctions comme premier paramètre. Ainsi, l’exemple suivant appelle la méthode **Read** d’un objet **pStream** :


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



En C + +, le pointeur vers la table de fonctions virtuelles, le pointeur *This* , est implicite. L’exemple suivant est équivalent à l’exemple précédent lors de l’utilisation de C + + :


```C++
pStream->Read(parameters) 
 
```



 

 




