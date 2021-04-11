---
title: Directives pragma
description: RC ne prend pas en charge les directives pragma prises en charge par le compilateur C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031217"
---
# <a name="pragma-directives"></a><span data-ttu-id="cf4c7-103">Directives pragma</span><span class="sxs-lookup"><span data-stu-id="cf4c7-103">Pragma Directives</span></span>

<span data-ttu-id="cf4c7-104">RC ne prend pas en charge les directives pragma prises en charge par le compilateur C/C++.</span><span class="sxs-lookup"><span data-stu-id="cf4c7-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="cf4c7-105">Toutefois, RC prend en charge la directive pragma suivante pour modifier la page de codes :</span><span class="sxs-lookup"><span data-stu-id="cf4c7-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="cf4c7-106">Ce pragma n’est pas pris en charge dans un fichier de ressources inclus (. RC).</span><span class="sxs-lookup"><span data-stu-id="cf4c7-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="cf4c7-107">Par conséquent, si vous avez un fichier. RC parent et qu’il inclut des fichiers. RC pour plusieurs langues, utilisez ce pragma avant d’inclure un autre fichier. RC plutôt que de l’utiliser dans le fichier. RC inclus.</span><span class="sxs-lookup"><span data-stu-id="cf4c7-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="cf4c7-108">Cette opération est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="cf4c7-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="cf4c7-109">Pour obtenir la liste des valeurs de CodePageNum, consultez [identificateurs de page de codes](../intl/code-page-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="cf4c7-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 