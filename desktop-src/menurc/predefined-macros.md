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
# <a name="predefined-macros"></a><span data-ttu-id="49453-104">Macros prédéfinies</span><span class="sxs-lookup"><span data-stu-id="49453-104">Predefined Macros</span></span>

<span data-ttu-id="49453-105">RC ne prend pas en charge les macros prédéfinies C ANSI (**\_ \_ date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ STDC \_ \_**, **\_ \_ Time \_ \_**, **\_ \_ timestamp \_ ). \_**</span><span class="sxs-lookup"><span data-stu-id="49453-105">RC does not support the ANSI C predefined macros (**\_\_DATE\_\_**, **\_\_FILE\_\_**, **\_\_LINE\_\_**, **\_\_STDC\_\_**, **\_\_TIME\_\_**, **\_\_TIMESTAMP\_\_**).</span></span> <span data-ttu-id="49453-106">Par conséquent, vous ne pouvez pas inclure ces macros dans les fichiers d’en-tête que vous incluez dans votre script de ressources.</span><span class="sxs-lookup"><span data-stu-id="49453-106">Therefore, you cannot include these macros in header files that you will include in your resource script.</span></span>

<span data-ttu-id="49453-107">RC définit la version RC \_ appelée, ce qui vous permet de compiler de façon conditionnelle des parties de vos fichiers d’en-tête, selon que le compilateur est votre compilateur C ou le compilateur RC.</span><span class="sxs-lookup"><span data-stu-id="49453-107">RC does define RC\_INVOKED, which enables you conditionally compile portions of your header files, depending on whether the compiler is your C compiler or the RC compiler.</span></span> <span data-ttu-id="49453-108">Cela est important, car le compilateur RC ne prend en charge qu’un sous-ensemble des instructions prises en charge par le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="49453-108">This is important because the RC compiler supports only a subset of the statements a C compiler would support.</span></span>

<span data-ttu-id="49453-109">Pour compiler de façon conditionnelle votre code avec le compilateur RC, entourez du code que RC ne peut pas compiler avec \# ifndef RC \_ invoked et **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="49453-109">To conditionally compile your code with the RC compiler, surround code that RC cannot compile with \#ifndef RC\_INVOKED and **\#endif**.</span></span>

<span data-ttu-id="49453-110">L’exemple suivant est extrait des exemples du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="49453-110">The following example is taken from the SDK samples.</span></span> <span data-ttu-id="49453-111">Il montre comment créer un fichier d’en-tête qui peut être compilé de manière conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="49453-111">It demonstrates how to create a header file that can be compiled conditionally.</span></span>

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




