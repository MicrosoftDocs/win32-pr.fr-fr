---
description: Méthode Delete de la classe Win32_SystemDriver-la suppression&\# 8194 ; La méthode de classe WMI supprime un service existant.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097087"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="b9946-103">Méthode Delete de la \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="b9946-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="b9946-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="b9946-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="b9946-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b9946-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b9946-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b9946-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9946-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9946-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="b9946-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9946-108">Parameters</span></span>

<span data-ttu-id="b9946-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9946-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9946-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9946-110">Return value</span></span>

<span data-ttu-id="b9946-111">Retourne la valeur 0 (zéro) si le service a été correctement supprimé, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b9946-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9946-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9946-112">Requirements</span></span>



| <span data-ttu-id="b9946-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9946-113">Requirement</span></span> | <span data-ttu-id="b9946-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9946-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9946-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9946-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b9946-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9946-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9946-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9946-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b9946-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9946-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9946-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b9946-119">Namespace</span></span><br/>                | <span data-ttu-id="b9946-120">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b9946-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9946-121">MOF</span><span class="sxs-lookup"><span data-stu-id="b9946-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9946-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9946-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9946-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b9946-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9946-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9946-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9946-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9946-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9946-126">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9946-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b9946-127">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="b9946-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

