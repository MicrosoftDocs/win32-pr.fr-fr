---
title: Macros prédéfinies
description: RC ne prend pas en charge les macros prédéfinies C ANSI ( \_ \_ date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ STDC \_ \_ , \_ \_ Time \_ \_ , \_ \_ timestamp \_ \_ ). Par conséquent, vous ne pouvez pas inclure ces macros dans les fichiers d’en-tête que vous incluez dans votre script de ressources.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9e48b915fae430bf776b9eebab7ac795e7b69a3d79e06a7ce6422b6d6eab6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971948"
---
# <a name="predefined-macros"></a>Macros prédéfinies

RC ne prend pas en charge les macros prédéfinies C ANSI (**\_ \_ date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ STDC \_ \_**, **\_ \_ Time \_ \_**, **\_ \_ timestamp \_ ). \_** Par conséquent, vous ne pouvez pas inclure ces macros dans les fichiers d’en-tête que vous incluez dans votre script de ressources.

RC définit la version RC \_ appelée, ce qui vous permet de compiler de façon conditionnelle des parties de vos fichiers d’en-tête, selon que le compilateur est votre compilateur C ou le compilateur RC. Cela est important, car le compilateur RC ne prend en charge qu’un sous-ensemble des instructions prises en charge par le compilateur C.

Pour compiler de façon conditionnelle votre code avec le compilateur RC, entourez du code que RC ne peut pas compiler avec \# ifndef RC \_ invoked et **\# endif**.

L’exemple suivant est extrait des exemples du kit de développement logiciel (SDK). Il montre comment créer un fichier d’en-tête qui peut être compilé de manière conditionnelle.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




