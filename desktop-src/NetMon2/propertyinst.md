---
description: La structure PROPERTYINST définit une instance d’une propriété dans une partie des données reconnues. Moniteur réseau alloue et remplit une structure PROPERTYINST lorsqu’une propriété est attachée à la capture.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: PROPERTYINST, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544807"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="0cc28-104">PROPERTYINST, structure</span><span class="sxs-lookup"><span data-stu-id="0cc28-104">PROPERTYINST structure</span></span>

<span data-ttu-id="0cc28-105">La structure **PROPERTYINST** définit une instance d’une propriété dans une partie des données reconnues.</span><span class="sxs-lookup"><span data-stu-id="0cc28-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="0cc28-106">Moniteur réseau alloue et remplit une structure **PROPERTYINST** lorsqu’une propriété est attachée à la capture.</span><span class="sxs-lookup"><span data-stu-id="0cc28-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc28-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cc28-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="0cc28-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0cc28-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0cc28-109">**lpPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0cc28-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-110">Pointeur vers la structure [PROPERTYINFO](propertyinfo.md) qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="0cc28-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-111">**szPropertyText**</span><span class="sxs-lookup"><span data-stu-id="0cc28-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-112">Pointeur vers une chaîne qui est affichée dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="0cc28-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-113">**lpData**</span><span class="sxs-lookup"><span data-stu-id="0cc28-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-114">Pointeur vers le début des données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0cc28-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="0cc28-115">L’analyseur détermine l’emplacement où les données de la propriété démarrent.</span><span class="sxs-lookup"><span data-stu-id="0cc28-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="0cc28-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-117">Pointeur vers les données d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="0cc28-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-118">**lpWord**</span><span class="sxs-lookup"><span data-stu-id="0cc28-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-119">Pointeur vers les données du **mot** .</span><span class="sxs-lookup"><span data-stu-id="0cc28-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-120">**lpDword**</span><span class="sxs-lookup"><span data-stu-id="0cc28-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-121">Pointeur vers les données **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0cc28-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-122">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="0cc28-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-123">Pointeur vers les données [**LARGEINT**](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc28-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-124">**lpSysTime**</span><span class="sxs-lookup"><span data-stu-id="0cc28-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-125">Pointeur vers les données [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="0cc28-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-126">**lpPropertyInstEx**</span><span class="sxs-lookup"><span data-stu-id="0cc28-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-127">Pointeur vers une structure [PROPERTYINSTEX](propertyinstex.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc28-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="0cc28-128">Le membre **lpPropertyInstEx** est utilisé uniquement lorsque vous appelez [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span><span class="sxs-lookup"><span data-stu-id="0cc28-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="0cc28-129">Si **lpPropertyInstEx** est utilisé, vous devez définir le membre **DATALENGTH** sur 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0cc28-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="0cc28-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-131">Longueur des données de cette instance de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0cc28-131">Data length for this instance of the property.</span></span> <span data-ttu-id="0cc28-132">Si le membre **lpPropertyInstEx** pointe vers une structure [**PROPERTYINSTEX**](propertyinstex.md) , vous devez affecter à **DATALENGTH** la valeur 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0cc28-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-133">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="0cc28-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-134">Informations de niveau.</span><span class="sxs-lookup"><span data-stu-id="0cc28-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="0cc28-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-136">Identificateur du contexte du fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="0cc28-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0cc28-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="0cc28-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0cc28-138">Indicateur de condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0cc28-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cc28-139">Notes</span><span class="sxs-lookup"><span data-stu-id="0cc28-139">Remarks</span></span>

<span data-ttu-id="0cc28-140">La structure **PROPERTYINST** définit une instance d’une propriété jointe.</span><span class="sxs-lookup"><span data-stu-id="0cc28-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="0cc28-141">L’analyseur accède à la structure **PROPERTYINST** par le biais de plusieurs fonctions d’assistance.</span><span class="sxs-lookup"><span data-stu-id="0cc28-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="0cc28-142">Par exemple, lorsque la fonction [**FormatPropertyInstance**](formatpropertyinstance.md) est appelée pour mettre en forme les données d’une propriété, elle modifie le membre **szPropertyText** de la structure **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="0cc28-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc28-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cc28-143">Requirements</span></span>



| <span data-ttu-id="0cc28-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cc28-144">Requirement</span></span> | <span data-ttu-id="0cc28-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cc28-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc28-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cc28-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc28-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cc28-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0cc28-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cc28-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc28-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cc28-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0cc28-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cc28-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc28-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc28-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc28-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cc28-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc28-153">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="0cc28-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="0cc28-154">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="0cc28-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

