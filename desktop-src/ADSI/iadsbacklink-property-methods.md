---
title: Méthodes de propriété IADsBackLink (IADs. h)
description: La méthode Property de l’interface IADsBackLink définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105157"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="246cb-105">Méthodes de propriété IADsBackLink</span><span class="sxs-lookup"><span data-stu-id="246cb-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="246cb-106">La méthode Property de l’interface [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="246cb-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="246cb-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="246cb-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="246cb-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="246cb-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="246cb-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="246cb-109">**ObjectName**</span></span>
<span data-ttu-id="246cb-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="246cb-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="246cb-111">Nom d’un objet auquel l’attribut de **lien précédent** est attaché.</span><span class="sxs-lookup"><span data-stu-id="246cb-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="246cb-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="246cb-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="246cb-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="246cb-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="246cb-114">**RemoteID**</span><span class="sxs-lookup"><span data-stu-id="246cb-114">**RemoteID**</span></span>
<span data-ttu-id="246cb-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="246cb-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="246cb-116">Identificateur du serveur distant qui requiert une référence externe de l’objet spécifié par **ObjectName**.</span><span class="sxs-lookup"><span data-stu-id="246cb-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="246cb-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="246cb-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="246cb-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="246cb-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="246cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="246cb-119">Requirements</span></span>



| <span data-ttu-id="246cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="246cb-120">Requirement</span></span> | <span data-ttu-id="246cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="246cb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="246cb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="246cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="246cb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="246cb-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="246cb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="246cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="246cb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="246cb-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="246cb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="246cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="246cb-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="246cb-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="246cb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="246cb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="246cb-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="246cb-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="246cb-130">IID</span><span class="sxs-lookup"><span data-stu-id="246cb-130">IID</span></span><br/>                      | <span data-ttu-id="246cb-131">IID \_ IADsBackLink est défini en tant que FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="246cb-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="246cb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="246cb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246cb-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="246cb-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="246cb-134">**\_lien secondaire ads**</span><span class="sxs-lookup"><span data-stu-id="246cb-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





