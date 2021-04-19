---
description: Représente un service de la plateforme Microsoft Windows Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Classe Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514989"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="4c401-103">MSVM \_ VirtualizationComponent, classe</span><span class="sxs-lookup"><span data-stu-id="4c401-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="4c401-104">Représente un service de la plateforme Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="4c401-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="4c401-105">La syntaxe suivante est simplifiée format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4c401-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c401-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c401-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="4c401-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4c401-107">Members</span></span>

<span data-ttu-id="4c401-108">La classe **MSVM \_ VirtualizationComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4c401-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4c401-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c401-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c401-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c401-110">Properties</span></span>

<span data-ttu-id="4c401-111">La classe **MSVM \_ VirtualizationComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c401-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c401-112">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="4c401-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c401-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c401-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c401-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c401-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c401-115">**GUID** qui représente l’identificateur de classe de l’objet com du service.</span><span class="sxs-lookup"><span data-stu-id="4c401-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="4c401-116">**Contexte**</span><span class="sxs-lookup"><span data-stu-id="4c401-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c401-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c401-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c401-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c401-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c401-119">Qualificateurs : **expérimental**</span><span class="sxs-lookup"><span data-stu-id="4c401-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="4c401-120">Contexte dans lequel l’objet nouvellement créé s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="4c401-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="4c401-121">Cette valeur est passée dans le paramètre *dwClsContext* à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="4c401-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="4c401-122">Cette propriété a toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="4c401-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4c401-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="4c401-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c401-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4c401-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4c401-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c401-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c401-126">**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="4c401-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="4c401-127">Cette propriété a toujours la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="4c401-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4c401-128">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4c401-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c401-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c401-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c401-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c401-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c401-131">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4c401-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4c401-132">Chaîne indépendante du langage qui identifie de façon unique le service.</span><span class="sxs-lookup"><span data-stu-id="4c401-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="4c401-133">Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ».</span><span class="sxs-lookup"><span data-stu-id="4c401-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="4c401-134">Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="4c401-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c401-135">Notes</span><span class="sxs-lookup"><span data-stu-id="4c401-135">Remarks</span></span>

<span data-ttu-id="4c401-136">L’accès à la classe **MSVM \_ VirtualizationComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4c401-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4c401-137">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4c401-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c401-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c401-138">Requirements</span></span>



| <span data-ttu-id="4c401-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c401-139">Requirement</span></span> | <span data-ttu-id="4c401-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c401-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c401-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c401-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4c401-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c401-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4c401-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c401-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4c401-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c401-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c401-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4c401-145">End of client support</span></span><br/>    | <span data-ttu-id="4c401-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4c401-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4c401-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4c401-147">End of server support</span></span><br/>    | <span data-ttu-id="4c401-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4c401-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4c401-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4c401-149">Namespace</span></span><br/>                | <span data-ttu-id="4c401-150">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4c401-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4c401-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4c401-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c401-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c401-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c401-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4c401-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c401-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c401-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

