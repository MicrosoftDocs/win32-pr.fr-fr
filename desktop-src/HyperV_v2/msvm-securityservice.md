---
description: Représente le service de sécurité. Il est utilisé pour configurer les paramètres de sécurité du système virtuel.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952125"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="ec325-104">MSVM \_ securityservice, classe</span><span class="sxs-lookup"><span data-stu-id="ec325-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="ec325-105">Représente le service de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ec325-105">Represents the security service.</span></span> <span data-ttu-id="ec325-106">Il est utilisé pour configurer les paramètres de sécurité du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec325-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="ec325-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ec325-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec325-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec325-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="ec325-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ec325-109">Members</span></span>

<span data-ttu-id="ec325-110">La classe **MSVM \_ securityservice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ec325-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="ec325-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ec325-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec325-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ec325-112">Methods</span></span>

<span data-ttu-id="ec325-113">La classe **MSVM \_ securityservice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ec325-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="ec325-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ec325-114">Method</span></span>                                                                                            | <span data-ttu-id="ec325-115">Description</span><span class="sxs-lookup"><span data-stu-id="ec325-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="ec325-116">**GetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="ec325-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="ec325-117">Méthode permettant de récupérer le protecteur de clé pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec325-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="ec325-118">**ModifySecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="ec325-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="ec325-119">Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec325-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="ec325-120">**RestoreLastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="ec325-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="ec325-121">Méthode pour restaurer le dernier protecteur de clé valide connu.</span><span class="sxs-lookup"><span data-stu-id="ec325-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="ec325-122">**SetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="ec325-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="ec325-123">Méthode permettant de définir le protecteur de clé pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec325-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="ec325-124">**SetSecurityPolicy**</span><span class="sxs-lookup"><span data-stu-id="ec325-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="ec325-125">Méthode permettant de définir le protecteur de clé pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec325-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="ec325-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ec325-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="ec325-127">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="ec325-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="ec325-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ec325-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="ec325-129">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="ec325-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="ec325-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec325-130">Requirements</span></span>



| <span data-ttu-id="ec325-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec325-131">Requirement</span></span> | <span data-ttu-id="ec325-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec325-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec325-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec325-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ec325-134">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec325-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ec325-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec325-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ec325-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ec325-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ec325-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec325-137">Namespace</span></span><br/>                | <span data-ttu-id="ec325-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec325-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec325-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ec325-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec325-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec325-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec325-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ec325-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec325-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec325-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec325-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec325-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec325-144">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="ec325-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




