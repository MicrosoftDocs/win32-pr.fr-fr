---
description: TAPI 1,4 a ajouté plusieurs API, messages, constantes et éléments de structure à la spécification 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951957"
---
# <a name="tapi-14"></a>TAPI 1,4

TAPI 1,4 a ajouté plusieurs API, messages, constantes et éléments de structure à la spécification 1,3. TAPI 1,4 prend en charge uniquement les TSPs 16 bits. Toutefois, il permet de développer des applications 32 bits sans avoir à se soucier des limitations de Windows 16 bits.

Les fichiers d’en-tête TAPI et TSPI sont utilisés pour développer les deux applications pour TAPI 1,4 et TAPI 2. x. Bien qu’il n’y avait pas beaucoup de modifications apportées aux structures entre ces deux spécifications, il y a eu des modifications apportées à l’API (notamment la prise en charge d’Unicode) qui rendent très important la compilation des en-têtes différemment, en fonction de la constante de la \_ version TAPI actuelle \_ . Par exemple :

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> La \_ version actuelle de l’interface TAPI \_ doit être définie pour toutes les applications TAPI. Bien qu’il ne soit pas strictement nécessaire pour le développement TAPI 2. x, il peut y avoir des modifications ultérieures.

 

 

 



