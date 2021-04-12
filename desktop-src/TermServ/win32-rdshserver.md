---
title: Classe Win32_RDSHServer
description: Gère un serveur hôte de session Bureau à distance.
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer de la classe Services Bureau à distance
- Win32_RDSHServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317265"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="517ce-105">\_Classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="517ce-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="517ce-106">Gère un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="517ce-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="517ce-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="517ce-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="517ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="517ce-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="517ce-109">Membres</span><span class="sxs-lookup"><span data-stu-id="517ce-109">Members</span></span>

<span data-ttu-id="517ce-110">La classe **Win32 \_ RDSHServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="517ce-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="517ce-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="517ce-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="517ce-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="517ce-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="517ce-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="517ce-113">Methods</span></span>

<span data-ttu-id="517ce-114">La classe **Win32 \_ RDSHServer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="517ce-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="517ce-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="517ce-115">Method</span></span>                                                                          | <span data-ttu-id="517ce-116">Description</span><span class="sxs-lookup"><span data-stu-id="517ce-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="517ce-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="517ce-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="517ce-118">Récupère une valeur de propriété entière d’un objet **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="517ce-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="517ce-119">**GetPendingStartServerList**</span><span class="sxs-lookup"><span data-stu-id="517ce-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="517ce-120">Récupère une liste de serveurs en attente de démarrage.</span><span class="sxs-lookup"><span data-stu-id="517ce-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="517ce-121">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="517ce-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="517ce-122">Récupère une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="517ce-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="517ce-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="517ce-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="517ce-124">Met à jour une valeur de propriété entière d’un objet **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="517ce-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="517ce-125">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="517ce-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="517ce-126">Met à jour une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="517ce-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="517ce-127">**TestAndSetState**</span><span class="sxs-lookup"><span data-stu-id="517ce-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="517ce-128">Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="517ce-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="517ce-129">Quelle que soit la correspondance, l’état actuel est également retourné.</span><span class="sxs-lookup"><span data-stu-id="517ce-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="517ce-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="517ce-130">Properties</span></span>

<span data-ttu-id="517ce-131">La classe **Win32 \_ RDSHServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="517ce-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="517ce-132">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="517ce-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ce-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="517ce-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ce-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="517ce-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517ce-135">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="517ce-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="517ce-136">Obtient et définit l’alias de la collection de serveurs d’hôtes de la hôte à laquelle le serveur hôte hôte est affecté.</span><span class="sxs-lookup"><span data-stu-id="517ce-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="517ce-137">**ConnectionBroker**</span><span class="sxs-lookup"><span data-stu-id="517ce-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ce-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="517ce-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ce-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="517ce-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="517ce-140">Obtient et définit le nom de l’Connexion Bureau à distance Broker (RDCB) qui gère l’accès des utilisateurs au serveur hôte hôte.</span><span class="sxs-lookup"><span data-stu-id="517ce-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="517ce-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="517ce-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ce-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="517ce-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ce-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="517ce-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517ce-144">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="517ce-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="517ce-145">Obtient et définit le nom du serveur de l’hôte de la configuration.</span><span class="sxs-lookup"><span data-stu-id="517ce-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="517ce-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="517ce-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ce-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="517ce-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="517ce-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="517ce-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ce-149">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="517ce-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="517ce-150">Décrit l’état du serveur.</span><span class="sxs-lookup"><span data-stu-id="517ce-150">Describes the state of the server.</span></span> <span data-ttu-id="517ce-151">Toute valeur autre que la **cible \_ en cours d’exécution** (3) est réservée et doit être prise en compte comme un État non valide.</span><span class="sxs-lookup"><span data-stu-id="517ce-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="517ce-152">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="517ce-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="517ce-153">**Cible \_ INCONNU** (1)</span><span class="sxs-lookup"><span data-stu-id="517ce-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="517ce-154">**Cible \_ En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="517ce-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="517ce-155">**Cible \_ NON valide** (8)</span><span class="sxs-lookup"><span data-stu-id="517ce-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="517ce-156">**Cible \_ DÉMARRAGE** (9)</span><span class="sxs-lookup"><span data-stu-id="517ce-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="517ce-157">**Cible \_ ARRÊT** (10)</span><span class="sxs-lookup"><span data-stu-id="517ce-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="517ce-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="517ce-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="517ce-159">**Windows server 2012 R2 et Windows server 2012 :** Cette propriété n’est pas disponible avant Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="517ce-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="517ce-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="517ce-160">Requirements</span></span>



| <span data-ttu-id="517ce-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="517ce-161">Requirement</span></span> | <span data-ttu-id="517ce-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="517ce-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="517ce-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="517ce-163">Minimum supported client</span></span><br/> | <span data-ttu-id="517ce-164">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="517ce-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="517ce-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="517ce-165">Minimum supported server</span></span><br/> | <span data-ttu-id="517ce-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="517ce-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="517ce-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="517ce-167">Namespace</span></span><br/>                | <span data-ttu-id="517ce-168">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="517ce-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="517ce-169">MOF</span><span class="sxs-lookup"><span data-stu-id="517ce-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="517ce-170"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="517ce-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="517ce-171">DLL</span><span class="sxs-lookup"><span data-stu-id="517ce-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="517ce-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="517ce-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="517ce-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="517ce-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517ce-174">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="517ce-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

