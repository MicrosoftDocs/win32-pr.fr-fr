---
title: Utilisation de plusieurs handles de contexte par appel
description: la possibilité d’utiliser des tableaux de handles de contexte en tant que paramètres est rendue disponible dans Windows Vista et les systèmes d’exploitation ultérieurs.
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7314d95847c438dc7620478b180919264948f8c171f3876b9b0ddd2f0b630689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010687"
---
# <a name="using-more-than-one-context-handle-per-call"></a>Utilisation de plusieurs handles de contexte par appel

la possibilité d’utiliser des tableaux de handles de contexte en tant que paramètres est rendue disponible dans Windows Vista et les systèmes d’exploitation ultérieurs. Toutefois, cette fonctionnalité doit être utilisée avec soin dans une application. Par exemple, dans une situation où un descripteur de contexte est utilisé dans plusieurs appels, il devient de plus en plus difficile d’assurer le suivi de son utilisation.

 

 




