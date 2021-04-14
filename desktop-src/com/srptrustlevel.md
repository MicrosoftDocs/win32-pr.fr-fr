---
title: SRPTrustLevel
description: Définit le niveau de confiance de la stratégie de restriction logicielle (SRP) pour les applications.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valeur de Registre SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379779"
---
# <a name="srptrustlevel"></a><span data-ttu-id="cf2bb-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="cf2bb-104">SRPTrustLevel</span></span>

<span data-ttu-id="cf2bb-105">Définit le niveau de confiance de la stratégie de restriction logicielle (SRP) pour les applications.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="cf2bb-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="cf2bb-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="cf2bb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cf2bb-107">Remarks</span></span>

<span data-ttu-id="cf2bb-108">Il s’agit d’une valeur **reg \_ DWORD** qui est disponible à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="cf2bb-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf2bb-109">Value</span></span>                                 | <span data-ttu-id="cf2bb-110">Description</span><span class="sxs-lookup"><span data-stu-id="cf2bb-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2bb-111">0x0 (sécurité \_ LEVELID non \_ autorisée)</span><span class="sxs-lookup"><span data-stu-id="cf2bb-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="cf2bb-112">L’accès à l’application et les privilèges utilisateur sensibles à la sécurité ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="cf2bb-113">0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED)</span><span class="sxs-lookup"><span data-stu-id="cf2bb-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="cf2bb-114">L’application dispose d’un accès illimité aux privilèges de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="cf2bb-115">Si la valeur **SRPTrustLevel** n’existe pas, la valeur par défaut sécurisée \_ LEVELID \_ interdit est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="cf2bb-116">Si **SRPTrustLevel** est de type incorrect ou hors limites, com renvoie l’erreur comadmin \_ E \_ SAFERINVALID.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="cf2bb-117">En cas d’échec de l’activation d’un tri en raison de vérifications d’approbation de SRP, COM renvoie l’erreur CO \_ E \_ ACTIVATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="cf2bb-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf2bb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf2bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf2bb-119">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="cf2bb-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="cf2bb-120">**SRPActivateAsActivatorChecks**</span><span class="sxs-lookup"><span data-stu-id="cf2bb-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="cf2bb-121">**SRPRunningObjectChecks**</span><span class="sxs-lookup"><span data-stu-id="cf2bb-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




