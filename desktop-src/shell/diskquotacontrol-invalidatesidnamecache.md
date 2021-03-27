---
description: Invalide le cache du nom d’utilisateur de l’ID de sécurité.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Méthode DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951017"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="a056c-103">Méthode DiskQuotaControl. InvalidateSidNameCache</span><span class="sxs-lookup"><span data-stu-id="a056c-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="a056c-104">Invalide le cache du nom d’utilisateur de l’ID de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a056c-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="a056c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a056c-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="a056c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a056c-106">Parameters</span></span>

<span data-ttu-id="a056c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a056c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a056c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a056c-108">Return value</span></span>

<span data-ttu-id="a056c-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a056c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a056c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a056c-110">Remarks</span></span>

<span data-ttu-id="a056c-111">Les noms d’utilisateur et les ID de sécurité associés sont stockés dans un cache.</span><span class="sxs-lookup"><span data-stu-id="a056c-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="a056c-112">Vous pouvez effacer ce cache en appelant **InvalidateSidNameCache**.</span><span class="sxs-lookup"><span data-stu-id="a056c-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="a056c-113">Si, par la suite, vous créez un nouvel objet utilisateur, les informations doivent être obtenues à partir du contrôleur de domaine, et le cache doit être rétabli.</span><span class="sxs-lookup"><span data-stu-id="a056c-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="a056c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a056c-114">Requirements</span></span>



| <span data-ttu-id="a056c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a056c-115">Requirement</span></span> | <span data-ttu-id="a056c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a056c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a056c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a056c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a056c-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a056c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a056c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a056c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a056c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a056c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a056c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a056c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a056c-122"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="a056c-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="a056c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a056c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a056c-124"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="a056c-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a056c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a056c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a056c-126">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="a056c-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




