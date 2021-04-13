---
title: Classe Win32_SessionDirectoryCluster
description: Fournit des propriétés pour l’affichage des propriétés d’une batterie de serveurs dans Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster de la classe Services Bureau à distance
- Win32_SessionDirectoryCluster de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464966"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="b2152-105">\_Classe SessionDirectoryCluster Win32</span><span class="sxs-lookup"><span data-stu-id="b2152-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="b2152-106">Fournit des propriétés pour l’affichage des propriétés d’une batterie de serveurs dans Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="b2152-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="b2152-107">Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b2152-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="b2152-108">Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="b2152-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b2152-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2152-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="b2152-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b2152-110">Members</span></span>

<span data-ttu-id="b2152-111">La classe **Win32 \_ SessionDirectoryCluster** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2152-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="b2152-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2152-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2152-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2152-113">Properties</span></span>

<span data-ttu-id="b2152-114">La classe **Win32 \_ SessionDirectoryCluster** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b2152-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2152-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="b2152-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2152-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2152-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2152-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2152-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2152-118">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2152-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2152-119">Nom de la batterie de serveurs du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b2152-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="b2152-120">**NumberOfServers**</span><span class="sxs-lookup"><span data-stu-id="b2152-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2152-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2152-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2152-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2152-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2152-123">Nombre de serveurs dans la batterie de serveurs du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b2152-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="b2152-124">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="b2152-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2152-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2152-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2152-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2152-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2152-127">Mode de session unique de la batterie de serveurs du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b2152-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="b2152-128">0</span><span class="sxs-lookup"><span data-stu-id="b2152-128">0</span></span>
</dt> <dd>

<span data-ttu-id="b2152-129">La batterie de serveurs du Service Broker pour les connexions Bureau à distance n’est pas en mode de session unique.</span><span class="sxs-lookup"><span data-stu-id="b2152-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="b2152-130">1</span><span class="sxs-lookup"><span data-stu-id="b2152-130">1</span></span>
</dt> <dd>

<span data-ttu-id="b2152-131">La batterie de serveurs du Service Broker pour les connexions Bureau à distance est en mode de session unique.</span><span class="sxs-lookup"><span data-stu-id="b2152-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2152-132">Notes</span><span class="sxs-lookup"><span data-stu-id="b2152-132">Remarks</span></span>

<span data-ttu-id="b2152-133">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b2152-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b2152-134">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b2152-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b2152-135">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b2152-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b2152-136">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b2152-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2152-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2152-137">Requirements</span></span>



| <span data-ttu-id="b2152-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2152-138">Requirement</span></span> | <span data-ttu-id="b2152-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2152-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2152-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2152-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b2152-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2152-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2152-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2152-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b2152-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2152-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b2152-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2152-144">Namespace</span></span><br/>                | <span data-ttu-id="b2152-145">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b2152-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="b2152-146">MOF</span><span class="sxs-lookup"><span data-stu-id="b2152-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2152-147"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2152-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2152-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b2152-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2152-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2152-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2152-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2152-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2152-151">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b2152-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="b2152-152">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="b2152-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

