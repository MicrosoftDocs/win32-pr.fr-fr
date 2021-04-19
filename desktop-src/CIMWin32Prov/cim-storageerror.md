---
description: La \_ classe CIM StorageError représente des blocs d’espace de média ou de mémoire qui sont mappés hors de l’utilisation en raison d’erreurs. La clé de la classe est la propriété de l’erreur de taille des octets erronés.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: Classe CIM_StorageError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517183"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="81405-104">\_Classe CIM StorageError</span><span class="sxs-lookup"><span data-stu-id="81405-104">CIM\_StorageError class</span></span>

<span data-ttu-id="81405-105">La classe **CIM \_ StorageError** représente des blocs d’espace de média ou de mémoire qui sont mappés hors de l’utilisation en raison d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="81405-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="81405-106">La clé de la classe est la **propriété de l’erreur** de taille des octets erronés.</span><span class="sxs-lookup"><span data-stu-id="81405-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81405-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="81405-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81405-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81405-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81405-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="81405-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="81405-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="81405-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81405-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81405-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="81405-112">Membres</span><span class="sxs-lookup"><span data-stu-id="81405-112">Members</span></span>

<span data-ttu-id="81405-113">La classe **CIM \_ StorageError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="81405-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="81405-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81405-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81405-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81405-115">Properties</span></span>

<span data-ttu-id="81405-116">La classe **CIM \_ StorageError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="81405-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81405-117">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81405-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="81405-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81405-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81405-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="81405-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="81405-121">Portée du nom de la classe de création de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="81405-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="81405-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="81405-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="81405-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81405-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81405-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**DeviceID**»)</span><span class="sxs-lookup"><span data-stu-id="81405-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="81405-126">Identificateur d’appareil de l’extension de stockage d’étendue.</span><span class="sxs-lookup"><span data-stu-id="81405-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="81405-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="81405-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81405-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81405-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81405-130">Adresse de fin des octets erronés.</span><span class="sxs-lookup"><span data-stu-id="81405-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="81405-131">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81405-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81405-132">**De la**</span><span class="sxs-lookup"><span data-stu-id="81405-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81405-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81405-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81405-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81405-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81405-136">Adresse de départ des octets erronés.</span><span class="sxs-lookup"><span data-stu-id="81405-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="81405-137">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81405-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81405-138">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81405-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="81405-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81405-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81405-141">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="81405-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="81405-142">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="81405-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="81405-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81405-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81405-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="81405-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81405-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81405-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81405-146">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemName**")</span><span class="sxs-lookup"><span data-stu-id="81405-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="81405-147">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="81405-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81405-148">Notes</span><span class="sxs-lookup"><span data-stu-id="81405-148">Remarks</span></span>

<span data-ttu-id="81405-149">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="81405-149">WMI does not implement this class.</span></span>

<span data-ttu-id="81405-150">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="81405-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81405-151">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="81405-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81405-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81405-152">Requirements</span></span>



| <span data-ttu-id="81405-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81405-153">Requirement</span></span> | <span data-ttu-id="81405-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="81405-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81405-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81405-155">Minimum supported client</span></span><br/> | <span data-ttu-id="81405-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81405-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81405-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81405-157">Minimum supported server</span></span><br/> | <span data-ttu-id="81405-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81405-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81405-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81405-159">Namespace</span></span><br/>                | <span data-ttu-id="81405-160">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="81405-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81405-161">MOF</span><span class="sxs-lookup"><span data-stu-id="81405-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81405-162"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81405-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81405-163">DLL</span><span class="sxs-lookup"><span data-stu-id="81405-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81405-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81405-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

