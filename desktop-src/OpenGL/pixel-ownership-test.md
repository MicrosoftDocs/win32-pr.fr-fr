---
title: Test de propriété des pixels
description: Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de traitement OpenGL, test de propriété de pixel
- test de propriété des pixels OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310337"
---
# <a name="pixel-ownership-test"></a>Test de propriété des pixels

Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier. Si c’est le cas, le fragment passe au test suivant. Si ce n’est pas le cas, le système de fenêtre détermine si le fragment est ignoré ou si d’autres opérations de fragment seront effectuées avec ce fragment. Avec ce test, le système de fenêtre contrôle le comportement quand, par exemple, une fenêtre OpenGL est masquée.

 

 




