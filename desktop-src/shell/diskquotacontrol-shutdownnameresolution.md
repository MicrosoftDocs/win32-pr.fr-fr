---
description: Arrête le thread de résolution de nom d’utilisateur.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Méthode DiskQuotaControl. ShutdownNameResolution (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033934"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="8c7b9-103">Méthode DiskQuotaControl. ShutdownNameResolution</span><span class="sxs-lookup"><span data-stu-id="8c7b9-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="8c7b9-104">Arrête le thread de résolution de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c7b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c7b9-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="8c7b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c7b9-106">Parameters</span></span>

<span data-ttu-id="8c7b9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c7b9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c7b9-108">Return value</span></span>

<span data-ttu-id="8c7b9-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7b9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8c7b9-110">Remarks</span></span>

<span data-ttu-id="8c7b9-111">Le programme de résolution de noms de l’identificateur de sécurité (SID) traduit le SID en noms d’utilisateur sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="8c7b9-112">Ce thread s’arrête automatiquement lorsque l’objet de contrôle de quota associé est détruit.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="8c7b9-113">Toutefois, dans certains cas, le thread n’est plus nécessaire, mais l’objet n’est pas encore prêt à être détruit.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="8c7b9-114">Un exemple typique est quand aucun traitement supplémentaire n’a lieu, mais les clients comportent toujours des références à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="8c7b9-115">La méthode **ShutdownNameResolution** vous permet de terminer le thread de résolution et de libérer les ressources associées sans détruire l’objet de contrôle de quota.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="8c7b9-116">Lorsque vous arrêtez le thread de résolution, la résolution de noms asynchrone s’arrête immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="8c7b9-117">Si des appels sont effectués par la suite sur des méthodes telles que [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md), l’objet quota peut recréer le thread de résolution.</span><span class="sxs-lookup"><span data-stu-id="8c7b9-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c7b9-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8c7b9-118">Requirements</span></span>



| <span data-ttu-id="8c7b9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c7b9-119">Requirement</span></span> | <span data-ttu-id="8c7b9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c7b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7b9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c7b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7b9-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c7b9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c7b9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c7b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7b9-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c7b9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8c7b9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c7b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c7b9-126"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c7b9-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="8c7b9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8c7b9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c7b9-128"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8c7b9-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c7b9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c7b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7b9-130">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8c7b9-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




