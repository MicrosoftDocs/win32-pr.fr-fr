---
title: show urlacl
description: Répertorie les listes DACL pour l’URL réservée spécifiée ou toutes les URL réservées.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- afficher urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103940519"
---
# <a name="show-urlacl"></a><span data-ttu-id="88334-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="88334-104">show urlacl</span></span>

<span data-ttu-id="88334-105">Répertorie les listes DACL pour l’URL réservée spécifiée ou toutes les URL réservées.</span><span class="sxs-lookup"><span data-stu-id="88334-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="88334-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88334-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88334-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* chaîne*</span><span class="sxs-lookup"><span data-stu-id="88334-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="88334-108">Spécifie l’URL complète.</span><span class="sxs-lookup"><span data-stu-id="88334-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="88334-109">S’il n’est pas spécifié, implique toutes les URL.</span><span class="sxs-lookup"><span data-stu-id="88334-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="88334-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="88334-110">Examples</span></span>

<span data-ttu-id="88334-111">**afficher l’URL de urlacl =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="88334-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="88334-112">**afficher l’URL de urlacl =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="88334-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




