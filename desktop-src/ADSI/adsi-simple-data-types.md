---
title: Types de données simples ADSI (IADs. h)
description: Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les types de données simples suivants.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032498"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="ad1c7-114">Types de données simples ADSI</span><span class="sxs-lookup"><span data-stu-id="ad1c7-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="ad1c7-115">Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les types de données simples suivants.</span><span class="sxs-lookup"><span data-stu-id="ad1c7-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="ad1c7-116">**\_BOOLÉENNE ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="ad1c7-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-118">**\_ \_ chaîne exacte de cas ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-120">**\_chaîne d' \_ ignorer le cas ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-122">**\_chaîne DN \_ ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-124">**\_entier ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="ad1c7-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-126">**\_grand \_ entier ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="ad1c7-127">**\_entier long**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="ad1c7-128">**\_chaîne numérique \_ ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-130">**\_classe d’objet ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-132">**\_chaînes imprimables \_ ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ad1c7-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-134">**\_handle de recherche ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="ad1c7-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="ad1c7-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="ad1c7-136">**\_heure UTC \_ ads**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="ad1c7-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="ad1c7-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad1c7-138">Notes</span><span class="sxs-lookup"><span data-stu-id="ad1c7-138">Remarks</span></span>

<span data-ttu-id="ad1c7-139">Lorsque ADSI lit un attribut qui a été défini en tant qu' **entier** dans le schéma LDAP, il gère toujours l’entier comme une valeur de 32 bits et peut tronquer les données.</span><span class="sxs-lookup"><span data-stu-id="ad1c7-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="ad1c7-140">Cela ne concerne que les serveurs LDAP qui autorisent des valeurs entières de taille arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ad1c7-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="ad1c7-141">Si l’attribut est un attribut personnalisé défini en étendant le schéma, vous pouvez éviter ce problème en définissant l’attribut personnalisé en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad1c7-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad1c7-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad1c7-142">Requirements</span></span>



| <span data-ttu-id="ad1c7-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad1c7-143">Requirement</span></span> | <span data-ttu-id="ad1c7-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad1c7-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ad1c7-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad1c7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ad1c7-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad1c7-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="ad1c7-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad1c7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ad1c7-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad1c7-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="ad1c7-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad1c7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad1c7-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad1c7-150"><dt>Iads.h</dt></span></span> </dl> |



 

