---
title: Valeurs de syntaxe simple SNMP (SNMP. h)
description: Les valeurs de syntaxe simple SNMP sont utilisées pour indiquer un type de variable SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104374"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="a72e9-103">Valeurs de syntaxe simple SNMP</span><span class="sxs-lookup"><span data-stu-id="a72e9-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="a72e9-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a72e9-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a72e9-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a72e9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a72e9-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a72e9-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a72e9-107">Les valeurs de syntaxe simple SNMP sont utilisées pour indiquer un type de variable SNMP.</span><span class="sxs-lookup"><span data-stu-id="a72e9-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="a72e9-108">Constante</span><span class="sxs-lookup"><span data-stu-id="a72e9-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="a72e9-109">Description</span><span class="sxs-lookup"><span data-stu-id="a72e9-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="a72e9-110"><dt>**\_entier ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="a72e9-111">Indique une variable entière signée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a72e9-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="a72e9-112"><dt>**\_bits ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="a72e9-113">Indique une variable qui est une énumération de bits nommés.</span><span class="sxs-lookup"><span data-stu-id="a72e9-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="a72e9-114"><dt>**\_OCTETSTRING ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="a72e9-115">Indique une variable de chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="a72e9-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="a72e9-116"><dt>**ASN \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="a72e9-117">Indique une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="a72e9-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="a72e9-118"><dt>**\_OBJECTIDENTIFIER ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="a72e9-119">Indique une variable d’identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="a72e9-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="a72e9-120"><dt>**\_INTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="a72e9-121">Indique une valeur entière signée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a72e9-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="a72e9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a72e9-122">Requirements</span></span>



| <span data-ttu-id="a72e9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a72e9-123">Requirement</span></span> | <span data-ttu-id="a72e9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a72e9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a72e9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a72e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a72e9-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a72e9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="a72e9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a72e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a72e9-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a72e9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a72e9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a72e9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a72e9-130"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a72e9-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72e9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a72e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72e9-132">Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)</span><span class="sxs-lookup"><span data-stu-id="a72e9-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="a72e9-133">Référence SNMP</span><span class="sxs-lookup"><span data-stu-id="a72e9-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="a72e9-134">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="a72e9-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

