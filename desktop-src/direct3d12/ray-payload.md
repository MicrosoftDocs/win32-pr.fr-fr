---
title: Structure de charge utile de rayon
description: Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel TraceRay, et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565629"
---
# <a name="ray-payload-structure"></a>Structure de charge utile de rayon 

Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel [**TraceRay**](traceray-function.md) , et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon, y compris [les](any-hit-shader.md)nuanceurs atteints, [atteints les plus proches](closest-hit-shader.md)et [manqués](miss-shader.md) . Les nuanceurs qui accèdent à la charge utile de rayon doivent utiliser la même structure que celle fournie lors de l’appel **TraceRay** d’origine.  Même si l’un de ces nuanceurs ne fait pas référence à la charge utile de rayon, il doit toujours spécifier la charge utile correspondante en tant qu’appel **TraceRay** d’origine.

