---
title: Macros prédéfinies
description: RC ne prend pas en charge les macros prédéfinies C ANSI ( \_ \_ date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ STDC \_ \_ , \_ \_ Time \_ \_ , \_ \_ timestamp \_ \_ ). Par conséquent, vous ne pouvez pas inclure ces macros dans les fichiers d’en-tête que vous incluez dans votre script de ressources.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100684"
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

 

 




