---
description: Traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Fonction RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110434"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="94410-103">RtlUnicodeToUTF8N fonction)</span><span class="sxs-lookup"><span data-stu-id="94410-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="94410-104">Traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="94410-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="94410-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94410-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="94410-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94410-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94410-107">*UTF8StringDestination* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="94410-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94410-108">Pointeur vers une mémoire tampon allouée par l’appelant pour recevoir la chaîne traduite.</span><span class="sxs-lookup"><span data-stu-id="94410-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="94410-109">*UTF8StringMaxByteCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94410-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94410-110">Nombre maximal d’octets à écrire dans *UTF8StringDestination*.</span><span class="sxs-lookup"><span data-stu-id="94410-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="94410-111">Si cette valeur provoque la troncation de la chaîne traduite, **RtlUnicodeToUTF8N** retourne un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="94410-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="94410-112">*UTF8StringActualByteCount* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="94410-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94410-113">Pointeur vers une variable allouée par l’appelant qui reçoit la longueur, en octets, de la chaîne traduite.</span><span class="sxs-lookup"><span data-stu-id="94410-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="94410-114">Ce paramètre est facultatif et peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="94410-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="94410-115">Si la chaîne est tronquée, le nombre retourné compte le nombre de chaînes tronquées réel.</span><span class="sxs-lookup"><span data-stu-id="94410-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="94410-116">*UnicodeStringSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94410-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94410-117">Pointeur vers la chaîne source Unicode à traduire.</span><span class="sxs-lookup"><span data-stu-id="94410-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="94410-118">\* UnicodeStringByteCount \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94410-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94410-119">Spécifie le nombre d’octets dans la chaîne source Unicode vers laquelle pointe le paramètre *UnicodeStringSource* .</span><span class="sxs-lookup"><span data-stu-id="94410-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94410-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94410-120">Return value</span></span>

<span data-ttu-id="94410-121">**RtlUnicodeToUTF8N** retourne l’une des valeurs NTSTATUS suivantes :</span><span class="sxs-lookup"><span data-stu-id="94410-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="94410-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="94410-122">Return code</span></span>                                                                                                  | <span data-ttu-id="94410-123">Description</span><span class="sxs-lookup"><span data-stu-id="94410-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94410-124"><dt>**État de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="94410-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="94410-125">La chaîne Unicode a été convertie en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="94410-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="94410-126"><dt>**ÉTAT \_ \_ non \_ mappé**</dt></span><span class="sxs-lookup"><span data-stu-id="94410-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="94410-127">Un caractère d’entrée non valide a été rencontré et remplacé.</span><span class="sxs-lookup"><span data-stu-id="94410-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="94410-128">Cet État est considéré comme un état de réussite.</span><span class="sxs-lookup"><span data-stu-id="94410-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="94410-129"><dt>**paramètre d’état \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94410-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="94410-130">Les deux pointeurs vers *UTF8StringDestination* et *UTF8StringActualByteCount* étaient **null**.</span><span class="sxs-lookup"><span data-stu-id="94410-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="94410-131"><dt>**Paramètre d’état \_ non valide \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="94410-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="94410-132">*UnicodeStringSource* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="94410-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="94410-133"><dt>**\_mémoire tampon d’état \_ trop \_ petite**</dt></span><span class="sxs-lookup"><span data-stu-id="94410-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="94410-134">*UTF8StringDestination* a été tronqué.</span><span class="sxs-lookup"><span data-stu-id="94410-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="94410-135">Notes</span><span class="sxs-lookup"><span data-stu-id="94410-135">Remarks</span></span>

<span data-ttu-id="94410-136">Bien que *UTF8StringActualByteCount* soit facultatif et peut avoir la **valeur null**, les appelants doivent fournir un stockage pour celui-ci, car la longueur reçue peut être utilisée pour déterminer si la conversion a réussi.</span><span class="sxs-lookup"><span data-stu-id="94410-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="94410-137">Cette routine ne modifie pas la chaîne source.</span><span class="sxs-lookup"><span data-stu-id="94410-137">This routine does not modify the source string.</span></span> <span data-ttu-id="94410-138">Elle retourne une chaîne UTF-8 terminée par le caractère NULL si le *UnicodeStringSource* donné a inclus un terminateur null et si le *UTF8StringMaxByteCount* donné n’a pas provoqué la troncation.</span><span class="sxs-lookup"><span data-stu-id="94410-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="94410-139">Si la sortie est tronquée et qu’un caractère d’entrée non valide est rencontré, la fonction retourne une \_ erreur de mémoire tampon d’état \_ insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="94410-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="94410-140">Si *UTF8StringDestination* a la valeur **null** , la fonction retourne le nombre d’octets requis pour héberger la chaîne traduite sans aucune troncation dans *UTF8StringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="94410-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="94410-141">Les appelants de **RtlUnicodeToUTF8N** doivent être exécutés au niveau IRQL < Dispatch \_ .</span><span class="sxs-lookup"><span data-stu-id="94410-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="94410-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94410-142">Requirements</span></span>



| <span data-ttu-id="94410-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94410-143">Requirement</span></span> | <span data-ttu-id="94410-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="94410-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94410-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94410-145">Minimum supported client</span></span><br/> | <span data-ttu-id="94410-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94410-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="94410-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94410-147">Minimum supported server</span></span><br/> | <span data-ttu-id="94410-148">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94410-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94410-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="94410-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="94410-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="94410-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="94410-151">DLL</span><span class="sxs-lookup"><span data-stu-id="94410-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94410-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94410-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94410-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94410-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94410-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="94410-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




