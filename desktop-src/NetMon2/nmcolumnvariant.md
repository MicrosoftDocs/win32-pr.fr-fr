---
description: Fournit une ligne dans le volet supérieur de la observateur d’événements qui sert de conteneur pour toutes les données possibles insérées dans une colonne.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: NMCOLUMNVARIANT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522001"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="f16d7-103">NMCOLUMNVARIANT, structure</span><span class="sxs-lookup"><span data-stu-id="f16d7-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="f16d7-104">La structure **NMCOLUMNVARIANT** fournit une ligne dans le volet supérieur de la observateur d’événements qui sert de conteneur pour toutes les données possibles insérées dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="f16d7-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f16d7-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="f16d7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f16d7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f16d7-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="f16d7-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-108">Valeur du type d’énumération [**NMCOLUMNTYPE**](nmcolumntype.md) .</span><span class="sxs-lookup"><span data-stu-id="f16d7-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f16d7-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f16d7-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-111">valeur de l’entier non signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-113">valeur de l’entier signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-115">valeur de l’entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-117">valeur de l’entier signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-119">valeur de l’entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-121">valeur de l’entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="f16d7-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-123">valeur flottante 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f16d7-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-124">**FrameVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-125">Numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="f16d7-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-126">**YesNoVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-127">Affiche Oui ou non.</span><span class="sxs-lookup"><span data-stu-id="f16d7-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-128">**OnOffVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-129">Affiche activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="f16d7-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-130">**TrueFalseVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-131">Affiche true ou false.</span><span class="sxs-lookup"><span data-stu-id="f16d7-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-132">**MACAddrVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-133">Adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="f16d7-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-134">**IPXAddrVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-135">Adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="f16d7-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-136">**IPAddrVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-137">Adresse IP.</span><span class="sxs-lookup"><span data-stu-id="f16d7-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-138">**VarTimeVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-139">Heure de la variante.</span><span class="sxs-lookup"><span data-stu-id="f16d7-139">Variant time.</span></span> <span data-ttu-id="f16d7-140">Utilisez **VariantTimetoSystemTime** pour effectuer la conversion en heure système.</span><span class="sxs-lookup"><span data-stu-id="f16d7-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="f16d7-141">**pStringVal**</span><span class="sxs-lookup"><span data-stu-id="f16d7-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="f16d7-142">Pointeur vers une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f16d7-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f16d7-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f16d7-143">Requirements</span></span>



| <span data-ttu-id="f16d7-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f16d7-144">Requirement</span></span> | <span data-ttu-id="f16d7-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f16d7-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f16d7-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16d7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f16d7-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16d7-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f16d7-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16d7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f16d7-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16d7-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f16d7-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="f16d7-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16d7-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16d7-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16d7-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f16d7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16d7-153">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="f16d7-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




