---
title: LegacyAuthenticationLevel
description: Définit le niveau d’authentification par défaut pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valeur de Registre LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029860"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="81492-104">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="81492-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="81492-105">Définit le niveau d’authentification par défaut pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="81492-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="81492-106">Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="81492-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="81492-107">Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="81492-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="81492-108">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="81492-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="81492-109">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="81492-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="81492-110">Notes</span><span class="sxs-lookup"><span data-stu-id="81492-110">Remarks</span></span>

<span data-ttu-id="81492-111">Il s’agit d’une valeur de **\_ mot reg** qui est équivalente aux \_ \_ constantes de niveau d’authentification RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="81492-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="81492-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="81492-112">Value</span></span> | <span data-ttu-id="81492-113">Constante</span><span class="sxs-lookup"><span data-stu-id="81492-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="81492-114">1</span><span class="sxs-lookup"><span data-stu-id="81492-114">1</span></span>     | <span data-ttu-id="81492-115">RPC \_ C \_ Authn \_ niveau \_ aucun</span><span class="sxs-lookup"><span data-stu-id="81492-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="81492-116">2</span><span class="sxs-lookup"><span data-stu-id="81492-116">2</span></span>     | <span data-ttu-id="81492-117">\_ \_ \_ connexion au niveau AUTHn C RPC \_</span><span class="sxs-lookup"><span data-stu-id="81492-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="81492-118">3</span><span class="sxs-lookup"><span data-stu-id="81492-118">3</span></span>     | <span data-ttu-id="81492-119">\_ \_ \_ appel au niveau d’authentification RPC C \_</span><span class="sxs-lookup"><span data-stu-id="81492-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="81492-120">4</span><span class="sxs-lookup"><span data-stu-id="81492-120">4</span></span>     | <span data-ttu-id="81492-121">protocole d’authentification de l' \_ authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="81492-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="81492-122">5</span><span class="sxs-lookup"><span data-stu-id="81492-122">5</span></span>     | <span data-ttu-id="81492-123">\_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_</span><span class="sxs-lookup"><span data-stu-id="81492-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="81492-124">6</span><span class="sxs-lookup"><span data-stu-id="81492-124">6</span></span>     | <span data-ttu-id="81492-125">\_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="81492-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="81492-126">Si cette valeur de Registre est absente, le niveau d’authentification par défaut établi par le système est 2 (RPC \_ C \_ Authn \_ Connect).</span><span class="sxs-lookup"><span data-stu-id="81492-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81492-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81492-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81492-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="81492-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="81492-129">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="81492-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="81492-130">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="81492-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




