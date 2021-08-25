---
title: Classes, objets et interfaces
description: Classes, objets et interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54008f316103a8a113e6702e4a4b1192bc0576f5a61fb28b38dbe2502bae881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786179"
---
# <a name="classes-objects-and-interfaces"></a>Classes, objets et interfaces

Dans le langage de programmation C++, une *classe* se compose de *Propriétés* (ou de données membres) et de *méthodes* (ou de fonctions membres). Les propriétés sont des éléments de données, tels que ceux contenus dans une structure. Les méthodes sont utilisées à diverses fins, telles que l’initialisation, l’assignation, les opérations et l’accès aux données. Vous utilisez une déclaration de classe de la même façon que vous utilisez une déclaration de structure. La mémoire est allouée pour une classe lorsque vous définissez un *objet* de classe. Chaque objet de classe a une zone de données pour ses propriétés et un tableau de pointeurs vers les méthodes qu’il prend en charge.

Dans OLE, un objet se compose de données et de méthodes, comme c’est le cas en C++. Toutefois, un objet OLE adhère à des règles plus strictes. Les données sont strictement internes. Un objet expose uniquement des interfaces. Une *interface* est un ensemble de méthodes associées pour un objet. Chaque objet peut prendre en charge plusieurs interfaces. Toutes les interfaces OLE prennent en charge l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

 

 




