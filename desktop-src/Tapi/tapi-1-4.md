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
# <a name="tapi-14"></a><span data-ttu-id="d2fd2-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="d2fd2-103">TAPI 1.4</span></span>

<span data-ttu-id="d2fd2-104">TAPI 1,4 a ajouté plusieurs API, messages, constantes et éléments de structure à la spécification 1,3.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="d2fd2-105">TAPI 1,4 prend en charge uniquement les TSPs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="d2fd2-106">Toutefois, il permet de développer des applications 32 bits sans avoir à se soucier des limitations de Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="d2fd2-107">Les fichiers d’en-tête TAPI et TSPI sont utilisés pour développer les deux applications pour TAPI 1,4 et TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="d2fd2-108">Bien qu’il n’y avait pas beaucoup de modifications apportées aux structures entre ces deux spécifications, il y a eu des modifications apportées à l’API (notamment la prise en charge d’Unicode) qui rendent très important la compilation des en-têtes différemment, en fonction de la constante de la \_ version TAPI actuelle \_ .</span><span class="sxs-lookup"><span data-stu-id="d2fd2-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="d2fd2-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d2fd2-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="d2fd2-110">La \_ version actuelle de l’interface TAPI \_ doit être définie pour toutes les applications TAPI.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="d2fd2-111">Bien qu’il ne soit pas strictement nécessaire pour le développement TAPI 2. x, il peut y avoir des modifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d2fd2-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



