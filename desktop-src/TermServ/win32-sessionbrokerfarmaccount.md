---
title: Classe Win32_SessionBrokerFarmAccount
description: La \_ classe SessionBrokerFarmAccount Win32 n’est plus disponible pour une utilisation à partir de Windows Server 2012. | Classe Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761851"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="56d36-106">\_Classe SessionBrokerFarmAccount Win32</span><span class="sxs-lookup"><span data-stu-id="56d36-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="56d36-107">\[La **classe \_ SessionBrokerFarmAccount Win32** n’est plus disponible pour une utilisation à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="56d36-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="56d36-108">Définit un compte de batterie session Broker.</span><span class="sxs-lookup"><span data-stu-id="56d36-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="56d36-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="56d36-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d36-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56d36-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="56d36-111">Membres</span><span class="sxs-lookup"><span data-stu-id="56d36-111">Members</span></span>

<span data-ttu-id="56d36-112">La classe **Win32 \_ SessionBrokerFarmAccount** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="56d36-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="56d36-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="56d36-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="56d36-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="56d36-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56d36-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="56d36-115">Methods</span></span>

<span data-ttu-id="56d36-116">La classe **Win32 \_ SessionBrokerFarmAccount** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="56d36-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="56d36-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="56d36-117">Method</span></span>                                                      | <span data-ttu-id="56d36-118">Description</span><span class="sxs-lookup"><span data-stu-id="56d36-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="56d36-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="56d36-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="56d36-120">Supprime le compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="56d36-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="56d36-121">Properties</span></span>

<span data-ttu-id="56d36-122">La classe **Win32 \_ SessionBrokerFarmAccount** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="56d36-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56d36-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="56d36-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="56d36-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56d36-126">Nom du domaine auquel appartient le compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="56d36-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="56d36-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56d36-130">Nom du compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-131">**AccountPassword**</span><span class="sxs-lookup"><span data-stu-id="56d36-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="56d36-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56d36-134">Mot de passe du compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="56d36-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56d36-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56d36-138">Premier nom de principal du service (SPN) associé au compte de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="56d36-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56d36-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56d36-142">Deuxième SPN associé au compte de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-143">**ComputerDNSName**</span><span class="sxs-lookup"><span data-stu-id="56d36-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="56d36-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56d36-146">Nom DNS de l’ordinateur associé au compte de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="56d36-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-147">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="56d36-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="56d36-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="56d36-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56d36-150">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="56d36-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="56d36-151">Nom de la batterie de serveurs session Broker.</span><span class="sxs-lookup"><span data-stu-id="56d36-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="56d36-152">**Manuel**</span><span class="sxs-lookup"><span data-stu-id="56d36-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d36-153">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="56d36-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56d36-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="56d36-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56d36-155">Indique si le mot de passe du compte est mis à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="56d36-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56d36-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56d36-156">Requirements</span></span>



| <span data-ttu-id="56d36-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56d36-157">Requirement</span></span> | <span data-ttu-id="56d36-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="56d36-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d36-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d36-159">Minimum supported client</span></span><br/> | <span data-ttu-id="56d36-160">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d36-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="56d36-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d36-161">Minimum supported server</span></span><br/> | <span data-ttu-id="56d36-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56d36-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="56d36-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="56d36-163">End of client support</span></span><br/>    | <span data-ttu-id="56d36-164">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d36-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="56d36-165">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="56d36-165">End of server support</span></span><br/>    | <span data-ttu-id="56d36-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56d36-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="56d36-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="56d36-167">Namespace</span></span><br/>                | <span data-ttu-id="56d36-168">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="56d36-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="56d36-169">MOF</span><span class="sxs-lookup"><span data-stu-id="56d36-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56d36-170"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56d36-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="56d36-171">DLL</span><span class="sxs-lookup"><span data-stu-id="56d36-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d36-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d36-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

