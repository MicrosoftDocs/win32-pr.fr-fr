---
description: Obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via les descripteurs de sécurité Windows n’est pas disponible.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: '__SystemSecurity :: Get9XUserList, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530151"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="df87d-103">\_\_SystemSecurity :: Get9XUserList, méthode</span><span class="sxs-lookup"><span data-stu-id="df87d-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="df87d-104">La méthode [**\_ \_ SystemSecurity :: Set9XUserList**](--systemsecurity-set9xuserlist.md) obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès par le biais de descripteurs de sécurité Windows n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="df87d-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="df87d-105">Cette fonction est similaire au descripteur de sécurité, mais elle est plus limitée.</span><span class="sxs-lookup"><span data-stu-id="df87d-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="df87d-106">Les groupes ne sont pas pris en charge et il n’y a aucun contrôle sur l’accès local, car l’utilisateur local a toujours un accès complet.</span><span class="sxs-lookup"><span data-stu-id="df87d-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="df87d-107">Refuser et autoriser les entrées de contrôle d’accès (ACE) sont autorisées, et pour cette raison, l’ordre d’accès est important dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="df87d-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="df87d-108">Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="df87d-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="df87d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df87d-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="df87d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df87d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df87d-111">*UL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df87d-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df87d-112">Tableau d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df87d-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df87d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df87d-113">Return value</span></span>

<span data-ttu-id="df87d-114">Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="df87d-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="df87d-115">La liste suivante répertorie les valeurs de retour dont l’importance est de **Get9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="df87d-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="df87d-116">Pour les scripts et les applications de Visual Basic, le résultat peut être [Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="df87d-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="df87d-117">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="df87d-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="df87d-118">**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="df87d-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="df87d-119">Cette méthode n’est pas prise en charge sur les versions prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="df87d-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df87d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df87d-120">Requirements</span></span>



| <span data-ttu-id="df87d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df87d-121">Requirement</span></span> | <span data-ttu-id="df87d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="df87d-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="df87d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df87d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df87d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df87d-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="df87d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df87d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df87d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df87d-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="df87d-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df87d-127">Namespace</span></span><br/>                | <span data-ttu-id="df87d-128">tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="df87d-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="df87d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df87d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df87d-130">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="df87d-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="df87d-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="df87d-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="df87d-132">**\_\_SystemSecurity :: est**</span><span class="sxs-lookup"><span data-stu-id="df87d-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="df87d-133">**\_\_SystemSecurity :: SetS**</span><span class="sxs-lookup"><span data-stu-id="df87d-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="df87d-134">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="df87d-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="df87d-135">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="df87d-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="df87d-136">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="df87d-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="df87d-137">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="df87d-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

