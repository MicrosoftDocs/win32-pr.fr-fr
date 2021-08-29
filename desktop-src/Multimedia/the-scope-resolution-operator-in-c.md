---
title: Opérateur de résolution de portée en C++
description: Opérateur de résolution de portée en C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf49d72288f43d8d27c1ea0238d072a61b6b708cf4dea812d00cc36193a11959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892539"
---
# <a name="the-scope-resolution-operator-in-c"></a>Opérateur de résolution de portée en C++

Deux signes deux-points ( ::) sont utilisés en C++ comme opérateur de *résolution de portée* . Cet opérateur vous offre plus de liberté pour nommer vos variables en vous permettant de faire la distinction entre les variables portant le même nom. Par exemple, *MyFile :: Read* fait référence à la méthode *Read* de la classe *MyFile* des objets, par opposition à *YourFile :: Read*, qui fait référence à une méthode *Read* dans la classe *YourFile* .

 

 




