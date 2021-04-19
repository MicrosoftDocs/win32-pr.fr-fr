---
title: ROTFlags
description: Contrôle l’inscription d’un serveur COM dans la table ROT (Running Object Table).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valeur de Registre ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508971"
---
# <a name="rotflags"></a><span data-ttu-id="323df-104">ROTFlags</span><span class="sxs-lookup"><span data-stu-id="323df-104">ROTFlags</span></span>

<span data-ttu-id="323df-105">Contrôle l’inscription d’un serveur COM dans la table ROT (Running Object Table).</span><span class="sxs-lookup"><span data-stu-id="323df-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="323df-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="323df-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="323df-107">Notes</span><span class="sxs-lookup"><span data-stu-id="323df-107">Remarks</span></span>

<span data-ttu-id="323df-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="323df-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="323df-109">Valeur de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="323df-109">Flag Value</span></span> | <span data-ttu-id="323df-110">Constante</span><span class="sxs-lookup"><span data-stu-id="323df-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="323df-111">0x1</span><span class="sxs-lookup"><span data-stu-id="323df-111">0x1</span></span>        | <span data-ttu-id="323df-112">**ROTREGFLAGS \_ ALLOWANYCLIENT**</span><span class="sxs-lookup"><span data-stu-id="323df-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="323df-113">Description de ROTREGFLAGS \_ ALLOWANYCLIENT</span><span class="sxs-lookup"><span data-stu-id="323df-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="323df-114">Si un serveur COM souhaite s’inscrire dans la table ROT et autoriser n’importe quel client à accéder à l’inscription, il doit utiliser l’indicateur **ROTFLAGS \_ ALLOWANYCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="323df-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="323df-115">Un serveur COM « Activate As Activator » ne peut pas spécifier **ROTFLAGS \_ ALLOWANYCLIENT** , car le gestionnaire de contrôle des services DCOM (DCOMSCM) applique un contrôle d’usurpation d’identité à cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="323df-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="323df-116">Par conséquent, dans Windows Vista et versions ultérieures, COM ajoute la prise en charge de l’entrée de Registre **ROTFlags** qui permet au serveur de stipuler que ses inscriptions rot sont mises à la disposition de n’importe quel client.</span><span class="sxs-lookup"><span data-stu-id="323df-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="323df-117">L’entrée doit exister dans la ruche **HKEY \_ local \_ machine** .</span><span class="sxs-lookup"><span data-stu-id="323df-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="323df-118">Cette entrée fournit un serveur « Activate As Activator » avec les mêmes fonctionnalités que celles fournies par **ROTFLAGS \_ ALLOWANYCLIENT** pour un serveur runas.</span><span class="sxs-lookup"><span data-stu-id="323df-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="323df-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="323df-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="323df-120">Clé AppID</span><span class="sxs-lookup"><span data-stu-id="323df-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="323df-121">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="323df-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="323df-122">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="323df-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




