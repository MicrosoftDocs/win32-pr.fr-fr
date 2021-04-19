---
title: LegacyImpersonationLevel
description: Définit le niveau d’emprunt d’identité par défaut pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valeur de Registre LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511221"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="be688-104">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="be688-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="be688-105">Définit le niveau d’emprunt d’identité par défaut pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="be688-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="be688-106">Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="be688-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="be688-107">Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="be688-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="be688-108">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="be688-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="be688-109">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="be688-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="be688-110">Notes</span><span class="sxs-lookup"><span data-stu-id="be688-110">Remarks</span></span>

<span data-ttu-id="be688-111">Il s’agit d’une valeur de **\_ mot reg** qui est équivalente aux \_ \_ constantes de niveau d’IMP RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="be688-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="be688-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="be688-112">Value</span></span> | <span data-ttu-id="be688-113">Constante</span><span class="sxs-lookup"><span data-stu-id="be688-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="be688-114">1</span><span class="sxs-lookup"><span data-stu-id="be688-114">1</span></span>     | <span data-ttu-id="be688-115">\_niveau d' \_ IMP \_ \_ anonyme du C RPC</span><span class="sxs-lookup"><span data-stu-id="be688-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="be688-116">2</span><span class="sxs-lookup"><span data-stu-id="be688-116">2</span></span>     | <span data-ttu-id="be688-117">\_identification du \_ niveau d’IMP RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="be688-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="be688-118">3</span><span class="sxs-lookup"><span data-stu-id="be688-118">3</span></span>     | <span data-ttu-id="be688-119">\_emprunt d' \_ identité du niveau d’IMP RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="be688-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="be688-120">4</span><span class="sxs-lookup"><span data-stu-id="be688-120">4</span></span>     | <span data-ttu-id="be688-121">\_délégué de \_ \_ niveau IMP RPC C \_</span><span class="sxs-lookup"><span data-stu-id="be688-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="be688-122">Si cette valeur de Registre est absente, le niveau d’emprunt d’identité par défaut établi par le système est 2 ( \_ identification du niveau d’IMP RPC C \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="be688-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be688-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be688-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be688-124">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="be688-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="be688-125">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="be688-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




