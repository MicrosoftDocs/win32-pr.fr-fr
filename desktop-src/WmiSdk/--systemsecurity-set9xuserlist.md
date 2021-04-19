---
description: Définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via les descripteurs de sécurité Windows n’est pas disponible.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: '__SystemSecurity :: Set9XUserList, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545059"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="0fc81-103">\_\_SystemSecurity :: Set9XUserList, méthode</span><span class="sxs-lookup"><span data-stu-id="0fc81-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="0fc81-104">La méthode **\_ \_ SystemSecurity :: Set9XUserList** définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès par le biais de descripteurs de sécurité Windows n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="0fc81-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="0fc81-105">La liste est spécifiée sous la forme d’un tableau d’objets incorporés où chaque objet est une instance de la classe [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) .</span><span class="sxs-lookup"><span data-stu-id="0fc81-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="0fc81-106">Cette fonction est similaire au descripteur de sécurité, mais elle est plus limitée.</span><span class="sxs-lookup"><span data-stu-id="0fc81-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="0fc81-107">Les groupes ne sont pas pris en charge et il n’y a aucun contrôle sur l’accès local, car l’utilisateur local a toujours un accès complet.</span><span class="sxs-lookup"><span data-stu-id="0fc81-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="0fc81-108">Refuser et autoriser les entrées de contrôle d’accès (ACE) sont autorisées, et pour cette raison, l’ordre d’accès est important dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="0fc81-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="0fc81-109">Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="0fc81-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc81-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fc81-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="0fc81-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fc81-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc81-112">*UL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fc81-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc81-113">Tableau d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0fc81-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc81-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fc81-114">Return value</span></span>

<span data-ttu-id="0fc81-115">Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0fc81-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="0fc81-116">La liste suivante répertorie les valeurs de retour dont l’importance est de **Set9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="0fc81-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="0fc81-117">Pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0fc81-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="0fc81-118">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0fc81-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="0fc81-119">**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="0fc81-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="0fc81-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0fc81-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fc81-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fc81-121">Requirements</span></span>



| <span data-ttu-id="0fc81-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fc81-122">Requirement</span></span> | <span data-ttu-id="0fc81-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fc81-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0fc81-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fc81-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc81-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fc81-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0fc81-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fc81-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc81-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fc81-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0fc81-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0fc81-128">Namespace</span></span><br/>                | <span data-ttu-id="0fc81-129">tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="0fc81-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0fc81-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fc81-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc81-131">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="0fc81-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0fc81-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="0fc81-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="0fc81-133">**\_\_SystemSecurity :: est**</span><span class="sxs-lookup"><span data-stu-id="0fc81-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="0fc81-134">**\_\_SystemSecurity :: SetS**</span><span class="sxs-lookup"><span data-stu-id="0fc81-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="0fc81-135">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="0fc81-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="0fc81-136">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="0fc81-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="0fc81-137">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="0fc81-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="0fc81-138">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="0fc81-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

