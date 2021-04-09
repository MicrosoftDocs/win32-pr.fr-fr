---
description: Les contextes d’application peuvent être utilisés pour créer des classes Windows côte à côte.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Création de classes Windows côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866022"
---
# <a name="creating-side-by-side-windows-classes"></a>Création de classes Windows côte à côte

Les contextes d’application peuvent être utilisés pour créer des classes Windows côte à côte. En utilisant des classes Windows côte à côte, votre application peut avoir des versions différentes d’une classe actives en même temps dans une fenêtre parente. Pour créer une classe Windows côte à côte, votre application doit activer un contexte d’activation avant d’appeler [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour obtenir un handle vers la nouvelle fenêtre.

Par exemple, les contrôles communs Windows version 5,82 et version 6,0 disposent tous les deux d’un contrôle d’édition. Windows utilise par défaut la version 5,82 du contrôle d’édition. Pour obtenir une fenêtre côte à côte avec la version 6,0 du contrôle d’édition, avant d’appeler [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) comme d’habitude, votre application peut référencer un assembly qui expose des classes de fenêtres nommées, puis activer le contexte d’activation qui référence les contrôles de la version 6,0.

 

 
