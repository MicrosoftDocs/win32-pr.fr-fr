---
title: Tables de fonctions virtuelles
description: Tables de fonctions virtuelles
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011712"
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



 

 




