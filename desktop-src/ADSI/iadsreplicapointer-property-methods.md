---
title: Méthodes de propriété IADsReplicaPointer (IADs. h)
description: La méthode Property de l’interface IADsReplicaPointer définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsReplicaPointer ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508498"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="7c4f6-105">Méthodes de propriété IADsReplicaPointer</span><span class="sxs-lookup"><span data-stu-id="7c4f6-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="7c4f6-106">La méthode Property de l’interface [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7c4f6-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="7c4f6-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7c4f6-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7c4f6-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c4f6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7c4f6-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-109">**Count**</span></span>
<span data-ttu-id="7c4f6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c4f6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c4f6-111">Nombre de réplicas existants.</span><span class="sxs-lookup"><span data-stu-id="7c4f6-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="7c4f6-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c4f6-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c4f6-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c4f6-114">**ReplicaAddressHints**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="7c4f6-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c4f6-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c4f6-116">Une adresse réseau est suggérée comme une référence probable à un nœud menant au serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="7c4f6-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="7c4f6-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c4f6-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c4f6-118">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c4f6-119">**ReplicaNumber**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-119">**ReplicaNumber**</span></span>
<span data-ttu-id="7c4f6-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c4f6-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c4f6-121">Numéro d’identification du réplica.</span><span class="sxs-lookup"><span data-stu-id="7c4f6-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="7c4f6-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c4f6-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c4f6-123">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c4f6-124">**ReplicaType**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-124">**ReplicaType**</span></span>
<span data-ttu-id="7c4f6-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c4f6-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c4f6-126">Type de réplica (maître, secondaire ou en lecture seule.)</span><span class="sxs-lookup"><span data-stu-id="7c4f6-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="7c4f6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c4f6-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c4f6-128">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c4f6-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-129">**ServerName**</span></span>
<span data-ttu-id="7c4f6-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c4f6-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c4f6-131">Nom du serveur de noms contenant le réplica.</span><span class="sxs-lookup"><span data-stu-id="7c4f6-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="7c4f6-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c4f6-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c4f6-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="7c4f6-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c4f6-134">Requirements</span></span>



| <span data-ttu-id="7c4f6-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c4f6-135">Requirement</span></span> | <span data-ttu-id="7c4f6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c4f6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4f6-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4f6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4f6-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c4f6-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c4f6-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4f6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4f6-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c4f6-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c4f6-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c4f6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4f6-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4f6-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7c4f6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7c4f6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c4f6-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c4f6-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c4f6-145">IID</span><span class="sxs-lookup"><span data-stu-id="7c4f6-145">IID</span></span><br/>                      | <span data-ttu-id="7c4f6-146">IID \_ IADsReplicaPointer est défini en tant que F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="7c4f6-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7c4f6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c4f6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4f6-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="7c4f6-149">**\_REPLICAPOINTER ads**</span><span class="sxs-lookup"><span data-stu-id="7c4f6-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





