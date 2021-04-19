---
title: Structure STOWED_EXCEPTION_INFORMATION_V2
description: Contient les informations sur les exceptions arrimées.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 structure Rapport d’erreurs Windows
- Pointeur de structure PSTOWED_EXCEPTION_INFORMATION_V2 Rapport d’erreurs Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510354"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="37d3e-105">Structure d' \_ informations d’exception de la \_ \_ version v2</span><span class="sxs-lookup"><span data-stu-id="37d3e-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="37d3e-106">Contient les informations sur les exceptions arrimées.</span><span class="sxs-lookup"><span data-stu-id="37d3e-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d3e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37d3e-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="37d3e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="37d3e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37d3e-109">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="37d3e-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-110">Type : **[ **\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-111">Structure d' [**\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md) qui contient des informations pour cette structure parente.</span><span class="sxs-lookup"><span data-stu-id="37d3e-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="37d3e-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="37d3e-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-113">Type : **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-114">Code [**HRESULT**](/windows/desktop/WinProg/windows-data-types) de l’exception arrimée.</span><span class="sxs-lookup"><span data-stu-id="37d3e-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="37d3e-115">**ExceptionForm**</span><span class="sxs-lookup"><span data-stu-id="37d3e-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-116">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-117">Valeur 2 bits qui identifie le formulaire de l’exception.</span><span class="sxs-lookup"><span data-stu-id="37d3e-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="37d3e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d3e-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="37d3e-119">Signification</span><span class="sxs-lookup"><span data-stu-id="37d3e-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="37d3e-120"><dt>**Rangé \_ \_ \_ Binaire de formulaire d’exception**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="37d3e-121">Cette valeur indique que la forme de l’exception est binaire.</span><span class="sxs-lookup"><span data-stu-id="37d3e-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="37d3e-122"><dt>**Rangé \_ \_ \_ Texte de formulaire d’exception**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="37d3e-123">Cette valeur indique que le formulaire de l’exception est du texte.</span><span class="sxs-lookup"><span data-stu-id="37d3e-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="37d3e-124">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="37d3e-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-125">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-126">Valeur de 30 bits qui identifie le thread qui a levé l’exception.</span><span class="sxs-lookup"><span data-stu-id="37d3e-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="37d3e-127">La valeur est décalée vers la droite de 2 bits lorsqu’elle est stockée.</span><span class="sxs-lookup"><span data-stu-id="37d3e-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="37d3e-128">Pour le reconvertir en un ID de thread valide, décalez la valeur vers la gauche de 2.</span><span class="sxs-lookup"><span data-stu-id="37d3e-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="37d3e-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="37d3e-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="37d3e-130">(*struct sans nom*)</span><span class="sxs-lookup"><span data-stu-id="37d3e-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-131">Les membres de cette structure imbriquée ne sont valides que si le membre **ExceptionForm** est défini sur le type d' **\_ exception \_ \_ arrimé**.</span><span class="sxs-lookup"><span data-stu-id="37d3e-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="37d3e-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="37d3e-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-133">Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-134">Pointeur qui contient l’adresse de l’exception.</span><span class="sxs-lookup"><span data-stu-id="37d3e-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="37d3e-135">**StackTraceWordSize**</span><span class="sxs-lookup"><span data-stu-id="37d3e-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-136">Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-137">Taille, en octets, de chaque mot de la trace de la pile vers lequel pointe le membre **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="37d3e-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="37d3e-138">Cette valeur est définie sur 4 pour les plateformes 32 bits et 8 pour les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37d3e-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="37d3e-139">**StackTraceWords**</span><span class="sxs-lookup"><span data-stu-id="37d3e-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-140">Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-141">Nombre de mots dans la trace de la pile vers lequel pointe le membre **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="37d3e-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="37d3e-142">Le nombre de mots est égal au nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="37d3e-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="37d3e-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="37d3e-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-144">Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-145">Pointeur vers un bloc de mémoire qui contient la trace de la pile.</span><span class="sxs-lookup"><span data-stu-id="37d3e-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="37d3e-146">(*struct sans nom*)</span><span class="sxs-lookup"><span data-stu-id="37d3e-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-147">Le membre de cette structure imbriquée est valide uniquement si le membre **ExceptionForm** est défini sur le **\_ \_ \_ texte de formulaire d’exception arrimé**.</span><span class="sxs-lookup"><span data-stu-id="37d3e-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="37d3e-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="37d3e-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-149">Type : **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-150">Pointeur vers une chaîne se terminant par un caractère null qui contient le texte d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="37d3e-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="37d3e-151">**NestedExceptionType**</span><span class="sxs-lookup"><span data-stu-id="37d3e-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-152">Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-153">Valeur 32 bits qui spécifie le type d’objet vers lequel pointe le membre **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="37d3e-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="37d3e-154">Définissez la valeur avec cette macro de définition de type d’échange d’octets qui suppose un faible endian :</span><span class="sxs-lookup"><span data-stu-id="37d3e-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="37d3e-155">Voici quelques définitions de type courantes :</span><span class="sxs-lookup"><span data-stu-id="37d3e-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="37d3e-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d3e-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="37d3e-157">Signification</span><span class="sxs-lookup"><span data-stu-id="37d3e-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="37d3e-158"><dt>**Rangé \_ \_Type imbriqué d' \_ exception \_ None**</dt> <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="37d3e-159">Cette valeur spécifie qu’il n’existe aucun objet exception imbriqué.</span><span class="sxs-lookup"><span data-stu-id="37d3e-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="37d3e-160"><dt>**Rangé \_ \_Type imbriqué d' \_ exception \_**</dt> type imbriqué <dt> \_ de l’exception Win32 \_ \_ ('W32E')</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="37d3e-161">Cette valeur spécifie que le membre **NestedException** pointe vers un objet [**\_ enregistrement d’exception**](/windows/desktop/api/winnt/ns-winnt-exception_record) .</span><span class="sxs-lookup"><span data-stu-id="37d3e-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="37d3e-162"><dt>**Rangé \_ exception \_ \_ \_**</dt> type imbriqué <dt>de l’exception arrimé de type imbriqué \_ \_ \_ ('arrim')</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="37d3e-163">Cette valeur spécifie que le membre **NestedException** pointe vers un autre objet exception rangé.</span><span class="sxs-lookup"><span data-stu-id="37d3e-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="37d3e-164">L’autre objet d’exception arrimée peut être un objet d’informations d’exception chargées **\_ \_ \_ v2** ou une version différente avec un membre d' **en-tête** valide, autrement dit un membre d' **en-tête** qui contient un [**\_ \_ \_ en-tête d’informations d’exception arrimé**](stowed-exception-information-header.md)valide.</span><span class="sxs-lookup"><span data-stu-id="37d3e-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="37d3e-165"><dt>**Rangé \_ Type imbriqué d’EXCEPTION type imbriqué de l’exception \_ \_ \_ CLR**</dt> <dt> \_ \_ \_ ('CLR1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="37d3e-166">Cette valeur spécifie que le membre **NestedException** pointe vers un objet d’exception « CLR1 ».</span><span class="sxs-lookup"><span data-stu-id="37d3e-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="37d3e-167"><dt>**Rangé \_ \_Type imbriqué d' \_ exception \_**</dt> type imbriqué <dt> \_ de l’exception Leo \_ \_ ('LEO1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="37d3e-168">Cette valeur spécifie que le membre **NestedException** pointe vers un objet d’exception de langage.</span><span class="sxs-lookup"><span data-stu-id="37d3e-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="37d3e-169">**NestedException**</span><span class="sxs-lookup"><span data-stu-id="37d3e-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="37d3e-170">Type : **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="37d3e-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="37d3e-171">Pointeur vers un type d’exception imbriquée.</span><span class="sxs-lookup"><span data-stu-id="37d3e-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="37d3e-172">Le type d’objet est indiqué par le membre **NestedExceptionType** .</span><span class="sxs-lookup"><span data-stu-id="37d3e-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37d3e-173">Notes</span><span class="sxs-lookup"><span data-stu-id="37d3e-173">Remarks</span></span>

<span data-ttu-id="37d3e-174">**Rangé \_ Les \_ informations \_ sur l’exception v2** et l' [**\_ \_ \_ en-tête d’informations d’exception arrimées**](stowed-exception-information-header.md) ne sont actuellement pas définis dans un en-tête disponible publiquement. vous devez donc les définir dans votre code source avant de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="37d3e-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="37d3e-175">La structure d’informations d’exception de la version **\_ \_ \_ v1** est identique à cette structure, sauf qu’elle ne contient pas les membres **NestedExceptionType** et **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="37d3e-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d3e-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d3e-176">Requirements</span></span>



| <span data-ttu-id="37d3e-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37d3e-177">Requirement</span></span> | <span data-ttu-id="37d3e-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d3e-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="37d3e-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d3e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="37d3e-180">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d3e-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37d3e-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d3e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="37d3e-182">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d3e-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="37d3e-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="37d3e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d3e-184"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="37d3e-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37d3e-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d3e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d3e-186">**enregistrement d’EXCEPTION \_**</span><span class="sxs-lookup"><span data-stu-id="37d3e-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="37d3e-187">**\_ \_ en-tête d’informations d’exception arrimé \_**</span><span class="sxs-lookup"><span data-stu-id="37d3e-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

