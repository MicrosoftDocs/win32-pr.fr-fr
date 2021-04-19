---
title: delete timeout
description: Supprime un délai d’attente global et rend le service HTTP.sys rétabli aux valeurs par défaut.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- supprimer le délai d’expiration HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106511057"
---
# <a name="delete-timeout"></a><span data-ttu-id="deb6c-104">delete timeout</span><span class="sxs-lookup"><span data-stu-id="deb6c-104">delete timeout</span></span>

<span data-ttu-id="deb6c-105">Supprime un délai d’attente global et rend le service HTTP.sys rétabli aux valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="deb6c-105">Deletes a global timeout and makes the HTTP.sys service revert to default values.</span></span>

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a><span data-ttu-id="deb6c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deb6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb6c-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout, \| HeaderWaitTimeout}**</span><span class="sxs-lookup"><span data-stu-id="deb6c-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="deb6c-108">Spécifie le type de paramètre de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="deb6c-108">Specifies the type of timeout setting.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="deb6c-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="deb6c-109">Examples</span></span>

<span data-ttu-id="deb6c-110">**delete timeout timeouttype=idleconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="deb6c-110">**delete timeout timeouttype=idleconnectiontimeout**</span></span>

<span data-ttu-id="deb6c-111">**delete timeout timeouttype=headerwaittimeout**</span><span class="sxs-lookup"><span data-stu-id="deb6c-111">**delete timeout timeouttype=headerwaittimeout**</span></span>

 

 




