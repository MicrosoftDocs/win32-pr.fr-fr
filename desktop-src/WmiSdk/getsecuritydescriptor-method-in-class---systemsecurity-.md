---
description: Obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté. Le descripteur de sécurité est retourné en tant qu’instance de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Méthode GetSecurityDescriptor de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522110"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="216a7-104">Méthode GetSecurityDescriptor de la \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="216a7-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="216a7-105">La méthode **GetSecurityDescriptor** obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="216a7-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="216a7-106">Le descripteur de sécurité est retourné en tant qu’instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="216a7-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="216a7-107">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="216a7-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="216a7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="216a7-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="216a7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="216a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216a7-110">*Descripteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="216a7-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="216a7-111">Descripteur de sécurité associé à l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="216a7-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216a7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="216a7-112">Return value</span></span>

<span data-ttu-id="216a7-113">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="216a7-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="216a7-114">Pour plus d’informations, consultez [codes de retour WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="216a7-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="216a7-115">**0**</span><span class="sxs-lookup"><span data-stu-id="216a7-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="216a7-116">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="216a7-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="216a7-117">**2**</span><span class="sxs-lookup"><span data-stu-id="216a7-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="216a7-118">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="216a7-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="216a7-119">**8**</span><span class="sxs-lookup"><span data-stu-id="216a7-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="216a7-120">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="216a7-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="216a7-121">**9**</span><span class="sxs-lookup"><span data-stu-id="216a7-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="216a7-122">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="216a7-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="216a7-123">**21**</span><span class="sxs-lookup"><span data-stu-id="216a7-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="216a7-124">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="216a7-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="216a7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="216a7-125">Remarks</span></span>

<span data-ttu-id="216a7-126">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="216a7-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="216a7-127">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="216a7-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="216a7-128">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="216a7-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="216a7-129">Pour plus d’informations, consultez [**constantes de privilège**](privilege-constants.md) et [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="216a7-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="216a7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="216a7-130">Requirements</span></span>



| <span data-ttu-id="216a7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="216a7-131">Requirement</span></span> | <span data-ttu-id="216a7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="216a7-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="216a7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216a7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="216a7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="216a7-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="216a7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216a7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="216a7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="216a7-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="216a7-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="216a7-137">Namespace</span></span><br/>                | <span data-ttu-id="216a7-138">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="216a7-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="216a7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="216a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216a7-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="216a7-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="216a7-141">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="216a7-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

