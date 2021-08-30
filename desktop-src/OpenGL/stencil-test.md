---
title: Test de stencil
description: Le test de stencil ignore conditionnellement un fragment en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon du stencil et une valeur de référence.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Pipeline de traitement OpenGL, test stencil
- test stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c35907a552861d504430bb412115bf05c9e1c09d183ca073e5f22d578ff726f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034589"
---
# <a name="stencil-test"></a>Test de stencil

Le test de stencil ignore conditionnellement un fragment en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon du stencil et une valeur de référence. La fonction [**glStencilFunc**](glstencilfunc.md) spécifie la fonction de comparaison et la valeur de référence. Si le fragment réussit ou échoue au test du stencil, la valeur dans la mémoire tampon du stencil est modifiée en fonction des instructions spécifiées par [**glStencilOp**](glstencilop.md).

 

 




