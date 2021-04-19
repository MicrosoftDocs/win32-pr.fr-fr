---
title: LegacySecureReferences
description: Détermine si les appels AddRef/Release sont sécurisés pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valeur de Registre LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508984"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="75ad4-104">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="75ad4-104">LegacySecureReferences</span></span>

<span data-ttu-id="75ad4-105">Détermine si les / appels de **version** de AddRef sont sécurisés pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="75ad4-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="75ad4-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="75ad4-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="75ad4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="75ad4-107">Remarks</span></span>

<span data-ttu-id="75ad4-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="75ad4-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="75ad4-109">La valeur « Y » ou « y » indiquent que **AddRef** et **Release** sont sécurisés.</span><span class="sxs-lookup"><span data-stu-id="75ad4-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="75ad4-110">Si cette valeur de Registre est absente ou est définie sur une valeur autre que « Y » ou « y », **AddRef** et **Release** ne sont pas sécurisés.</span><span class="sxs-lookup"><span data-stu-id="75ad4-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="75ad4-111">L’activation de références sécurisées ralentit les appels distants.</span><span class="sxs-lookup"><span data-stu-id="75ad4-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ad4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75ad4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ad4-113">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="75ad4-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="75ad4-114">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="75ad4-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




