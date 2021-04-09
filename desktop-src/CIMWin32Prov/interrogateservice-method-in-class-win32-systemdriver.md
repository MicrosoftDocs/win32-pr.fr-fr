---
description: Demande que le service du pilote système met à jour son état sur Service Manager.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Méthode InterrogateService de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110487"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="862f4-103">Méthode InterrogateService de la \_ classe Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="862f4-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="862f4-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** demande que le service du pilote système met à jour son état avec Service Manager.</span><span class="sxs-lookup"><span data-stu-id="862f4-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="862f4-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="862f4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="862f4-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="862f4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="862f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="862f4-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="862f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="862f4-108">Parameters</span></span>

<span data-ttu-id="862f4-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="862f4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="862f4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="862f4-110">Return value</span></span>

<span data-ttu-id="862f4-111">Retourne la valeur 0 (zéro) si la demande **InterrogateService** a été acceptée, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="862f4-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="862f4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="862f4-112">Requirements</span></span>



| <span data-ttu-id="862f4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="862f4-113">Requirement</span></span> | <span data-ttu-id="862f4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="862f4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="862f4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="862f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="862f4-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="862f4-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="862f4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="862f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="862f4-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="862f4-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="862f4-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="862f4-119">Namespace</span></span><br/>                | <span data-ttu-id="862f4-120">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="862f4-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="862f4-121">MOF</span><span class="sxs-lookup"><span data-stu-id="862f4-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="862f4-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="862f4-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="862f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="862f4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="862f4-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="862f4-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862f4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="862f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862f4-126">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="862f4-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="862f4-127">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="862f4-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="862f4-128">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="862f4-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

