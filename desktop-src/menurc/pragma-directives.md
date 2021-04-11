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
# <a name="pragma-directives"></a>Directives pragma

RC ne prend pas en charge les directives pragma prises en charge par le compilateur C/C++. Toutefois, RC prend en charge la directive pragma suivante pour modifier la page de codes :

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Ce pragma n’est pas pris en charge dans un fichier de ressources inclus (. RC). Par conséquent, si vous avez un fichier. RC parent et qu’il inclut des fichiers. RC pour plusieurs langues, utilisez ce pragma avant d’inclure un autre fichier. RC plutôt que de l’utiliser dans le fichier. RC inclus. Cette opération est illustrée dans l’exemple suivant.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Pour obtenir la liste des valeurs de CodePageNum, consultez [identificateurs de page de codes](../intl/code-page-identifiers.md).

 

 