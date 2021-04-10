---
description: Convertit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Fonction RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200937"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="887f6-103">RtlUTF8ToUnicodeN fonction)</span><span class="sxs-lookup"><span data-stu-id="887f6-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="887f6-104">Convertit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="887f6-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="887f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="887f6-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="887f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="887f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887f6-107">*UnicodeStringDestination* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="887f6-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="887f6-108">Pointeur vers une mémoire tampon allouée par l’appelant qui reçoit la chaîne traduite.</span><span class="sxs-lookup"><span data-stu-id="887f6-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="887f6-109">*UnicodeStringMaxByteCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="887f6-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887f6-110">Nombre maximal d’octets à écrire dans *UnicodeStringDestination*.</span><span class="sxs-lookup"><span data-stu-id="887f6-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="887f6-111">Si cette valeur provoque la troncation de la chaîne traduite, **RtlUTF8ToUnicodeN** retourne un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="887f6-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="887f6-112">*UnicodeStringActualByteCount* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="887f6-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="887f6-113">Pointeur vers une variable allouée par l’appelant qui reçoit la longueur, en octets, de la chaîne traduite.</span><span class="sxs-lookup"><span data-stu-id="887f6-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="887f6-114">Ce paramètre est facultatif et peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="887f6-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="887f6-115">Si la chaîne est tronquée, le nombre retourné compte le nombre de chaînes tronquées réel.</span><span class="sxs-lookup"><span data-stu-id="887f6-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="887f6-116">*UTF8StringSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="887f6-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887f6-117">Pointeur vers la chaîne à traduire.</span><span class="sxs-lookup"><span data-stu-id="887f6-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="887f6-118">*UTF8StringByteCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="887f6-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887f6-119">Taille, en octets, de la chaîne sur *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="887f6-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887f6-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="887f6-120">Return value</span></span>

<span data-ttu-id="887f6-121">**RtlUTF8ToUnicodeN** retourne l’une des valeurs NTSTATUS suivantes :</span><span class="sxs-lookup"><span data-stu-id="887f6-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="887f6-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="887f6-122">Return code</span></span>                                                                                                  | <span data-ttu-id="887f6-123">Description</span><span class="sxs-lookup"><span data-stu-id="887f6-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="887f6-124"><dt>**État de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="887f6-125">La chaîne a été convertie en Unicode.</span><span class="sxs-lookup"><span data-stu-id="887f6-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="887f6-126"><dt>**ÉTAT \_ \_ non \_ mappé**</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="887f6-127">Un caractère d’entrée non valide a été rencontré et remplacé.</span><span class="sxs-lookup"><span data-stu-id="887f6-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="887f6-128">Cet État est considéré comme un état de réussite.</span><span class="sxs-lookup"><span data-stu-id="887f6-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="887f6-129"><dt>**paramètre d’état \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="887f6-130">Les deux pointeurs vers *UnicodeStringDestination* et *UnicodeStringActualByteCount* étaient **null**.</span><span class="sxs-lookup"><span data-stu-id="887f6-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="887f6-131"><dt>**Paramètre d’état \_ non valide \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="887f6-132">*UTF8StringSource* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="887f6-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="887f6-133"><dt>**\_mémoire tampon d’état \_ trop \_ petite**</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="887f6-134">*UnicodeStringDestination* a été tronqué.</span><span class="sxs-lookup"><span data-stu-id="887f6-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="887f6-135">Notes</span><span class="sxs-lookup"><span data-stu-id="887f6-135">Remarks</span></span>

<span data-ttu-id="887f6-136">Bien que *UnicodeStringActualByteCount* soit facultatif et peut avoir la **valeur null**, les appelants doivent fournir un stockage pour celui-ci, car la longueur reçue peut être utilisée pour déterminer si la conversion a réussi.</span><span class="sxs-lookup"><span data-stu-id="887f6-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="887f6-137">Si la sortie est tronquée et qu’un caractère d’entrée non valide est rencontré, la fonction retourne une \_ erreur de mémoire tampon d’état \_ insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="887f6-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="887f6-138">Si *UnicodeStringDestination* a la valeur **null** , la fonction retourne le nombre d’octets requis pour héberger la chaîne traduite sans aucune troncation dans *UnicodeStringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="887f6-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="887f6-139">**RtlUTF8ToUnicodeN** ne modifie pas la chaîne source, sauf si les pointeurs *UnicodeStringDestination* et *UTF8StringSource* sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="887f6-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="887f6-140">La chaîne Unicode retournée n’est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="887f6-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="887f6-141">Les appelants de **RtlUTF8ToUnicodeN** doivent être exécutés au niveau IRQL < Dispatch \_ .</span><span class="sxs-lookup"><span data-stu-id="887f6-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="887f6-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="887f6-142">Requirements</span></span>



| <span data-ttu-id="887f6-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="887f6-143">Requirement</span></span> | <span data-ttu-id="887f6-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="887f6-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="887f6-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887f6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="887f6-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="887f6-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="887f6-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887f6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="887f6-148">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="887f6-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="887f6-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="887f6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="887f6-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="887f6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="887f6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887f6-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887f6-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887f6-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="887f6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887f6-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="887f6-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




