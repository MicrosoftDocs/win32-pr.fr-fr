---
description: Définit un objet unique d’un filtre d’affichage.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: FILTEROBJECT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519254"
---
# <a name="filterobject-structure"></a><span data-ttu-id="da7dd-103">FILTEROBJECT, structure</span><span class="sxs-lookup"><span data-stu-id="da7dd-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="da7dd-104">La structure **FILTEROBJECT** définit un objet unique d’un filtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="da7dd-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="da7dd-105">La fonction [**FilterAddObject**](filteraddobject.md) utilise **FILTEROBJECT** pour créer un filtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="da7dd-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="da7dd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da7dd-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="da7dd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="da7dd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="da7dd-108">**Action**</span><span class="sxs-lookup"><span data-stu-id="da7dd-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-109">Indicateur qui spécifie l’action **FILTEROBJECT** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="da7dd-110">Un indicateur peut spécifier une propriété, une valeur ou un opérateur.</span><span class="sxs-lookup"><span data-stu-id="da7dd-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="da7dd-111">Le tableau suivant répertorie les indicateurs de propriété de membre d’action.</span><span class="sxs-lookup"><span data-stu-id="da7dd-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="da7dd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7dd-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="da7dd-113">Signification</span><span class="sxs-lookup"><span data-stu-id="da7dd-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="da7dd-114"><dt>**FILTERACTION ( \_ propriété)**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="da7dd-115">Contient cette propriété.</span><span class="sxs-lookup"><span data-stu-id="da7dd-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="da7dd-116"><dt>**FILTERACTION \_ PROPERTYEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="da7dd-117">Indique qu’une propriété d’action de filtre est déjà définie.</span><span class="sxs-lookup"><span data-stu-id="da7dd-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="da7dd-118">Le tableau suivant répertorie les indicateurs de valeur de membre d’action.</span><span class="sxs-lookup"><span data-stu-id="da7dd-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="da7dd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7dd-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="da7dd-120">Signification</span><span class="sxs-lookup"><span data-stu-id="da7dd-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="da7dd-121"><dt>**valeur de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="da7dd-122">Contient cette valeur.</span><span class="sxs-lookup"><span data-stu-id="da7dd-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="da7dd-123"><dt>**chaîne de filtrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="da7dd-124">Contient cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="da7dd-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="da7dd-125"><dt>**Groupe de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="da7dd-126">Contient ce tableau.</span><span class="sxs-lookup"><span data-stu-id="da7dd-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="da7dd-127"><dt>**FILTERACTION \_ CONTAINSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="da7dd-128">Indique qu’une propriété contient une sous-chaîne non sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="da7dd-129"><dt>**l’action de filtrage \_ contient**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="da7dd-130">Indique qu’une propriété contient une sous-chaîne respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="da7dd-131"><dt>**adresse de filtrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="da7dd-132">Contient l’adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="da7dd-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="da7dd-133"><dt>**FILTERACTION \_ ADDRESSANY**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="da7dd-134">Correspond à n’importe quelle adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="da7dd-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="da7dd-135"><dt>**ACTION \_ de filtrage à partir de**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="da7dd-136">Indique l’adresse **Mac de** l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="da7dd-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="da7dd-137"><dt>**ACTION \_ de filtrage vers**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="da7dd-138">Indique l’adresse **Mac** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="da7dd-139"><dt>**FILTERACTION \_ FROMTO**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="da7dd-140">Indique un jumelage de **/à** des adresses Mac.</span><span class="sxs-lookup"><span data-stu-id="da7dd-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="da7dd-141"><dt>**FILTERACTION \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="da7dd-142">Contient un entier long.</span><span class="sxs-lookup"><span data-stu-id="da7dd-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="da7dd-143"><dt>**heure de l’action de filtrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="da7dd-144">Contient une structure **SystemTime** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="da7dd-145"><dt>**ACTION de filtrage d' \_ adresse \_ éther**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="da7dd-146">Contient une adresse MAC Ethernet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="da7dd-147"><dt>**\_jeton d’adresse de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="da7dd-148">Contient une adresse MAC Token Ring.</span><span class="sxs-lookup"><span data-stu-id="da7dd-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="da7dd-149"><dt>**ACTION de filtrage d' \_ adresse \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="da7dd-150">Contient une adresse MAC FDDI.</span><span class="sxs-lookup"><span data-stu-id="da7dd-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="da7dd-151"><dt>**adresse de filtrage d’adresses \_ \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="da7dd-152">Contient une adresse MAC IPX.</span><span class="sxs-lookup"><span data-stu-id="da7dd-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="da7dd-153"><dt>**adresse IP de l’adresse de filtrage \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="da7dd-154">Contient une adresse MAC IP.</span><span class="sxs-lookup"><span data-stu-id="da7dd-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="da7dd-155"><dt>**OID de filtrage \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="da7dd-156">Contient un identificateur d’objet (OID).</span><span class="sxs-lookup"><span data-stu-id="da7dd-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="da7dd-157">Le tableau suivant répertorie les indicateurs d’opérateur de membre d’action.</span><span class="sxs-lookup"><span data-stu-id="da7dd-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="da7dd-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7dd-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="da7dd-159">Signification</span><span class="sxs-lookup"><span data-stu-id="da7dd-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="da7dd-160"><dt>**ACTION de filtrage \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="da7dd-161">Indique une action de filtre non valide.</span><span class="sxs-lookup"><span data-stu-id="da7dd-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="da7dd-162"><dt>**FILTERACTION \_ et**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="da7dd-163">Indique une instruction **and** logique.</span><span class="sxs-lookup"><span data-stu-id="da7dd-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="da7dd-164"><dt>**FILTERACTION \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="da7dd-165">Indique une instruction **or** logique.</span><span class="sxs-lookup"><span data-stu-id="da7dd-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="da7dd-166"><dt>**FILTERACTION \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="da7dd-167">Indique une instruction **or** exclusive logique (XOR).</span><span class="sxs-lookup"><span data-stu-id="da7dd-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="da7dd-168"><dt>**ACTION \_ non**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="da7dd-169">Indique une instruction **not** logique.</span><span class="sxs-lookup"><span data-stu-id="da7dd-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="da7dd-170"><dt>**FILTERACTION \_ EQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="da7dd-171">L’action de filtrage est égale et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="da7dd-172"><dt>**ACTION de filtrage \_ égale**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="da7dd-173">L’action de filtrage est égale à et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="da7dd-174"><dt>**FILTERACTION \_ NOTEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="da7dd-175">L’instruction not logique est égale à et **ne respecte pas** la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="da7dd-176"><dt>**FILTERACTION \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="da7dd-177">L’instruction **not** logique est EQUAL et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="da7dd-178"><dt>**FILTERACTION \_ GREATERNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="da7dd-179">L’action de filtrage est supérieure à (>) et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="da7dd-180"><dt>**ACTION de filtrage \_ supérieure**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="da7dd-181">L’action de filtrage est supérieure à (>) et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="da7dd-182"><dt>**FILTERACTION \_ LESSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="da7dd-183">L’action de filtrage est inférieure à (<) et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="da7dd-184"><dt>**ACTION de filtrage \_ moins**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="da7dd-185">L’action de filtrage est inférieure à (<) et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="da7dd-186"><dt>**FILTERACTION \_ GREATEREQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="da7dd-187">L’action de filtrage est supérieure ou égale à (>=) et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="da7dd-188"><dt>**FILTERACTION \_ greaterequal à**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="da7dd-189">L’action de filtrage est supérieure ou égale à (>=) et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="da7dd-190"><dt>**FILTERACTION \_ LESSEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="da7dd-191">L’action de filtrage est inférieure ou égale à (<=) et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="da7dd-192"><dt>**FILTERACTION \_ LESSEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="da7dd-193">L’action de filtrage est inférieure ou égale à (<=) et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="da7dd-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="da7dd-194"><dt>**ACTION de filtrage \_ plus**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="da7dd-195">Ajoutez l’opérateur (+).</span><span class="sxs-lookup"><span data-stu-id="da7dd-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="da7dd-196"><dt>**ACTION de filtrage \_ moins**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="da7dd-197">Opérateur de soustraction (-).</span><span class="sxs-lookup"><span data-stu-id="da7dd-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="da7dd-198"><dt>**FILTERACTION \_ AREBITSON**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="da7dd-199">Indique une opération au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="da7dd-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="da7dd-200"><dt>**FILTERACTION \_ AREBITSOFF**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="da7dd-201">Indique une opération non-au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="da7dd-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="da7dd-202"><dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="da7dd-203">Indique que les protocoles sélectionnés existent.</span><span class="sxs-lookup"><span data-stu-id="da7dd-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="da7dd-204"><dt>**FILTERACTION \_ PROTOCOLEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="da7dd-205">Indique que le protocole sélectionné existe.</span><span class="sxs-lookup"><span data-stu-id="da7dd-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="da7dd-206"><dt>**FILTERACTION \_ ARRAYEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="da7dd-207">Indique que le contenu du tableau est égal.</span><span class="sxs-lookup"><span data-stu-id="da7dd-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="da7dd-208">L’indicateur doit être utilisé avec une structure de **\_ tableau de FILTERACTION** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="da7dd-209"><dt>**FILTERACTION \_ DEREFPROPERTY**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="da7dd-210">Décrit une correspondance de modèle à un offset (en octets) à partir du protocole.</span><span class="sxs-lookup"><span data-stu-id="da7dd-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="da7dd-211"><dt>**l' \_ OID de FILTERACTION \_ contient**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="da7dd-212">Évalue une sous-chaîne dans un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="da7dd-213">L’action doit être utilisée avec la structure de l' **\_ OID de FILTERACTION** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="da7dd-214"><dt>**l' \_ OID \_ de FILTERACTION commence \_ par**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="da7dd-215">Évalue une sous-chaîne qui commence un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="da7dd-216">L’indicateur doit être utilisé avec **l' \_ OID de FILTERACTION**.</span><span class="sxs-lookup"><span data-stu-id="da7dd-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="da7dd-217"><dt>**l' \_ OID \_ de filtrage se termine \_ par**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="da7dd-218">Évalue une sous-chaîne qui termine un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="da7dd-219">L’indicateur doit être utilisé avec **l' \_ OID de FILTERACTION**.</span><span class="sxs-lookup"><span data-stu-id="da7dd-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="da7dd-220"><dt>**ACTION de filtrage des \_ \_ vignes**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="da7dd-221">Contient une adresse MAC Vines.</span><span class="sxs-lookup"><span data-stu-id="da7dd-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="da7dd-222"><dt>**EXPRESSION de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="da7dd-223">Contient une expression d’action.</span><span class="sxs-lookup"><span data-stu-id="da7dd-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="da7dd-224"><dt>**FILTERACTION (valeur \_ booléenne)**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="da7dd-225">Contient un type de données **bool** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="da7dd-226"><dt>**DIRECTION du filtre \_ \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="da7dd-227">Contrôle la direction séquentielle (Frame suivant) dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="da7dd-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="da7dd-228"><dt>**DIRECTION du filtre \_ \_ préc.**</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="da7dd-229">Contrôle la direction séquentielle (Frame précédent) dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="da7dd-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="da7dd-230">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="da7dd-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-231">Handle d’une clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="da7dd-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-232">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="da7dd-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-233">Valeur d’un objet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-234">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="da7dd-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-235">Handle permettant d’afficher le protocole de filtre.</span><span class="sxs-lookup"><span data-stu-id="da7dd-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="da7dd-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-237">Pointeur vers un tableau.</span><span class="sxs-lookup"><span data-stu-id="da7dd-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-238">**lpProtocolTable**</span><span class="sxs-lookup"><span data-stu-id="da7dd-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-239">Pointeur vers une liste de protocoles conçue pour tester l’existence d’un protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="da7dd-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="da7dd-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-241">Pointeur vers l’adresse du type de noyau.</span><span class="sxs-lookup"><span data-stu-id="da7dd-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="da7dd-242">Par exemple, MAC ou IP.</span><span class="sxs-lookup"><span data-stu-id="da7dd-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-243">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="da7dd-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-244">Double **DWORD** utilisé dans une application Windows NT ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="da7dd-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-245">**lpTime**</span><span class="sxs-lookup"><span data-stu-id="da7dd-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-246">Pointeur vers une structure **SystemTime** .</span><span class="sxs-lookup"><span data-stu-id="da7dd-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-247">**lpOID**</span><span class="sxs-lookup"><span data-stu-id="da7dd-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-248">Pointeur vers la structure de l' **\_ identificateur d’objet** (OID).</span><span class="sxs-lookup"><span data-stu-id="da7dd-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="da7dd-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-250">Nombre, en octets, dans le frame.</span><span class="sxs-lookup"><span data-stu-id="da7dd-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-251">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="da7dd-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-252">Valeur d’octet de décalage de la structure FILTEROBJECT utilisée pour comparer des tableaux.</span><span class="sxs-lookup"><span data-stu-id="da7dd-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="da7dd-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="da7dd-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="da7dd-254">Réservé.</span><span class="sxs-lookup"><span data-stu-id="da7dd-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da7dd-255">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da7dd-255">Requirements</span></span>



| <span data-ttu-id="da7dd-256">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da7dd-256">Requirement</span></span> | <span data-ttu-id="da7dd-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7dd-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da7dd-258">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da7dd-258">Minimum supported client</span></span><br/> | <span data-ttu-id="da7dd-259">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da7dd-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da7dd-260">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da7dd-260">Minimum supported server</span></span><br/> | <span data-ttu-id="da7dd-261">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da7dd-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da7dd-262">En-tête</span><span class="sxs-lookup"><span data-stu-id="da7dd-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="da7dd-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="da7dd-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




