---
title: Méthodes de propriété IADsAcl (IADs. h)
description: La méthode Property de l’interface IADsAcl définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsAcl ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466247"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="c1597-105">Méthodes de propriété IADsAcl</span><span class="sxs-lookup"><span data-stu-id="c1597-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="c1597-106">La méthode Property de l’interface [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c1597-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="c1597-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c1597-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c1597-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c1597-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c1597-109">**Privilèges**</span><span class="sxs-lookup"><span data-stu-id="c1597-109">**Privileges**</span></span>
<span data-ttu-id="c1597-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c1597-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c1597-111">Paramètres des privilèges.</span><span class="sxs-lookup"><span data-stu-id="c1597-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="c1597-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1597-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c1597-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="c1597-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1597-114">**ProtectedAttrName**</span><span class="sxs-lookup"><span data-stu-id="c1597-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="c1597-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c1597-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c1597-116">Nom d’un attribut protégé.</span><span class="sxs-lookup"><span data-stu-id="c1597-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="c1597-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1597-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c1597-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c1597-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1597-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="c1597-119">**SubjectName**</span></span>
<span data-ttu-id="c1597-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c1597-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="c1597-121">Nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c1597-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="c1597-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c1597-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c1597-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c1597-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="c1597-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1597-124">Requirements</span></span>



| <span data-ttu-id="c1597-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1597-125">Requirement</span></span> | <span data-ttu-id="c1597-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1597-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1597-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1597-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1597-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1597-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1597-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1597-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1597-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1597-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1597-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1597-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1597-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1597-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c1597-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c1597-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1597-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1597-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1597-135">IID</span><span class="sxs-lookup"><span data-stu-id="c1597-135">IID</span></span><br/>                      | <span data-ttu-id="c1597-136">IID \_ IADsAcl est défini en tant que 8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c1597-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="c1597-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1597-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1597-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="c1597-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





