---
description: La fonction AuthzFreeCentralAccessPolicyCallback est une fonction définie par l’application qui libère de la mémoire allouée par la fonction AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: AuthzFreeCentralAccessPolicyCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211082"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="12422-103">AuthzFreeCentralAccessPolicyCallback fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="12422-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="12422-104">La fonction *AuthzFreeCentralAccessPolicyCallback* est une fonction définie par l’application qui libère de la mémoire allouée par la fonction [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) .</span><span class="sxs-lookup"><span data-stu-id="12422-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="12422-105">*AuthzFreeCentralAccessPolicyCallback* est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="12422-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="12422-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12422-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="12422-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12422-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12422-108">*pCentralAccessPolicy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12422-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12422-109">Pointeur vers la stratégie d’accès centralisée à libérer.</span><span class="sxs-lookup"><span data-stu-id="12422-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12422-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12422-110">Return value</span></span>

<span data-ttu-id="12422-111">Si la fonction est réussie, la fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="12422-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="12422-112">Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="12422-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="12422-113">Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="12422-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="12422-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12422-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12422-115">**\_informations d’initialisation authment \_**</span><span class="sxs-lookup"><span data-stu-id="12422-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="12422-116">*AuthzGetCentralAccessPolicyCallback*</span><span class="sxs-lookup"><span data-stu-id="12422-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
