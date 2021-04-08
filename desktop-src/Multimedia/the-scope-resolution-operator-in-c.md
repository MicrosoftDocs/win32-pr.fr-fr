---
title: Opérateur de résolution de portée en C++
description: Opérateur de résolution de portée en C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840086"
---
# <a name="the-scope-resolution-operator-in-c"></a>Opérateur de résolution de portée en C++

Deux signes deux-points ( ::) sont utilisés en C++ comme opérateur de *résolution de portée* . Cet opérateur vous offre plus de liberté pour nommer vos variables en vous permettant de faire la distinction entre les variables portant le même nom. Par exemple, *MyFile :: Read* fait référence à la méthode *Read* de la classe *MyFile* des objets, par opposition à *YourFile :: Read*, qui fait référence à une méthode *Read* dans la classe *YourFile* .

 

 




