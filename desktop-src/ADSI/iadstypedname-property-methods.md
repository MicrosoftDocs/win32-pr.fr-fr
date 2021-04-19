---
title: Méthodes de propriété IADsTypedName (IADs. h)
description: La méthode Property de l’interface IADsTypedName définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsTypedName ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511555"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="633fa-105">Méthodes de propriété IADsTypedName</span><span class="sxs-lookup"><span data-stu-id="633fa-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="633fa-106">La méthode Property de l’interface [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="633fa-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="633fa-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="633fa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="633fa-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="633fa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="633fa-109">**Intervalle**</span><span class="sxs-lookup"><span data-stu-id="633fa-109">**Interval**</span></span>
<span data-ttu-id="633fa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="633fa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="633fa-111">Fréquence de référence de l’objet.</span><span class="sxs-lookup"><span data-stu-id="633fa-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="633fa-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="633fa-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633fa-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="633fa-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="633fa-114">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="633fa-114">**Level**</span></span>
<span data-ttu-id="633fa-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="633fa-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="633fa-116">Niveau de priorité associé à l’objet.</span><span class="sxs-lookup"><span data-stu-id="633fa-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="633fa-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="633fa-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633fa-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="633fa-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="633fa-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="633fa-119">**ObjectName**</span></span>
<span data-ttu-id="633fa-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="633fa-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="633fa-121">Nom d’un objet.</span><span class="sxs-lookup"><span data-stu-id="633fa-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="633fa-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="633fa-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633fa-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="633fa-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="633fa-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="633fa-124">Requirements</span></span>



| <span data-ttu-id="633fa-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="633fa-125">Requirement</span></span> | <span data-ttu-id="633fa-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="633fa-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="633fa-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="633fa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="633fa-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="633fa-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="633fa-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="633fa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="633fa-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="633fa-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="633fa-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="633fa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="633fa-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="633fa-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="633fa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="633fa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633fa-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633fa-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="633fa-135">IID</span><span class="sxs-lookup"><span data-stu-id="633fa-135">IID</span></span><br/>                      | <span data-ttu-id="633fa-136">IID \_ IADsTypedName est défini en tant que B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="633fa-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="633fa-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="633fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633fa-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="633fa-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="633fa-139">**\_TYPEDNAME ads**</span><span class="sxs-lookup"><span data-stu-id="633fa-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





