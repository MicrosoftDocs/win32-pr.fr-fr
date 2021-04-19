---
title: delete cache
description: Vide l’intégralité du cache d’URL ou supprime les entrées en fonction de l’URL spécifiée.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- supprimer le cache HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106512706"
---
# <a name="delete-cache"></a><span data-ttu-id="d058b-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="d058b-104">delete cache</span></span>

<span data-ttu-id="d058b-105">Vide l’intégralité du cache d’URL ou supprime les entrées en fonction de l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d058b-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="d058b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d058b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d058b-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* chaîne*</span><span class="sxs-lookup"><span data-stu-id="d058b-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="d058b-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d058b-108">Required.</span></span> <span data-ttu-id="d058b-109">Spécifie l’URL complète.</span><span class="sxs-lookup"><span data-stu-id="d058b-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="d058b-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[récursif = \] {Oui \| non}**</span><span class="sxs-lookup"><span data-stu-id="d058b-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="d058b-111">Si c’est le cas, supprime toutes les entrées sous l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d058b-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d058b-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="d058b-112">Examples</span></span>

<span data-ttu-id="d058b-113">**supprimer l’URL du cache = https://www.contoso.com:80/myresource/ recursive = Oui**</span><span class="sxs-lookup"><span data-stu-id="d058b-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




