---
title: Structure de charge utile de rayon
description: Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel TraceRay, et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106523099"
---
# <a name="ray-payload-structure"></a>Structure de charge utile de rayon 

Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel [**TraceRay**](traceray-function.md) , et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon, y compris [les](any-hit-shader.md)nuanceurs atteints, [atteints les plus proches](closest-hit-shader.md)et [manqués](miss-shader.md) . Les nuanceurs qui accèdent à la charge utile de rayon doivent utiliser la même structure que celle fournie lors de l’appel **TraceRay** d’origine.  Même si l’un de ces nuanceurs ne fait pas référence à la charge utile de rayon, il doit toujours spécifier la charge utile correspondante en tant qu’appel **TraceRay** d’origine.

