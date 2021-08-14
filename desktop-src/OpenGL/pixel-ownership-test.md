---
title: Test de propriété des pixels
description: Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de traitement OpenGL, test de propriété de pixel
- test de propriété des pixels OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cfefe133b3951fa70d51736f664ec5a7cb9942c4c05f892115dd222013f294
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936248"
---
# <a name="pixel-ownership-test"></a>Test de propriété des pixels

Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier. Si c’est le cas, le fragment passe au test suivant. Si ce n’est pas le cas, le système de fenêtre détermine si le fragment est ignoré ou si d’autres opérations de fragment seront effectuées avec ce fragment. Avec ce test, le système de fenêtre contrôle le comportement quand, par exemple, une fenêtre OpenGL est masquée.

 

 




