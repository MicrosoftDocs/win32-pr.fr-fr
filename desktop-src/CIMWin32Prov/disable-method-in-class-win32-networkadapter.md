---
description: Désactive la carte réseau.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Désactivation de la méthode de la classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532071"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="6da26-103">Disable, méthode de la \_ classe NetworkAdapter Win32</span><span class="sxs-lookup"><span data-stu-id="6da26-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="6da26-104">La méthode **Disable** désactive la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="6da26-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6da26-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="6da26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6da26-106">Parameters</span></span>

<span data-ttu-id="6da26-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6da26-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6da26-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6da26-108">Return value</span></span>

<span data-ttu-id="6da26-109">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6da26-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="6da26-110">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="6da26-110">Any other number indicates an error.</span></span> <span data-ttu-id="6da26-111">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6da26-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="6da26-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6da26-112">Requirements</span></span>



| <span data-ttu-id="6da26-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6da26-113">Requirement</span></span> | <span data-ttu-id="6da26-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6da26-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da26-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da26-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6da26-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6da26-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6da26-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da26-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6da26-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6da26-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6da26-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6da26-119">Namespace</span></span><br/>                | <span data-ttu-id="6da26-120">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6da26-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6da26-121">MOF</span><span class="sxs-lookup"><span data-stu-id="6da26-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6da26-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6da26-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6da26-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6da26-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da26-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da26-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da26-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6da26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da26-126">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="6da26-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="6da26-127">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="6da26-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="6da26-128">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="6da26-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

