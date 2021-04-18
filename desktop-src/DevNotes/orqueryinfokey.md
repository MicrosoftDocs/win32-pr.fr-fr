---
description: Récupère des informations sur la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: ORQueryInfoKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533144"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="30dd9-103">ORQueryInfoKey fonction)</span><span class="sxs-lookup"><span data-stu-id="30dd9-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="30dd9-104">Récupère des informations sur la clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="30dd9-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="30dd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30dd9-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="30dd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30dd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30dd9-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="30dd9-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-109">*lpClass* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-110">Pointeur vers une mémoire tampon qui reçoit la classe de clé.</span><span class="sxs-lookup"><span data-stu-id="30dd9-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="30dd9-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-112">*lpcClass* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-113">Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpClass* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="30dd9-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="30dd9-114">La taille doit inclure le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-114">The size should include the terminating null character.</span></span> <span data-ttu-id="30dd9-115">Quand la fonction retourne une valeur, cette variable contient la taille de la chaîne de classe qui est stockée dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="30dd9-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="30dd9-116">Le nombre retourné n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="30dd9-117">Si la mémoire tampon n’est pas assez grande, la fonction retourne l’erreur \_ plus \_ de données et la variable contient la taille de la chaîne, en caractères, sans compter le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="30dd9-118">Si *lpClass* a la **valeur null**, *LpcClass* peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="30dd9-119">Si le paramètre *lpClass* est une adresse valide, mais que le paramètre *lpcClass* n’est pas (par exemple, si le paramètre *lpcClass* a la **valeur null**), la fonction retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="30dd9-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-120">*lpcSubKeys* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-121">Pointeur vers une variable qui reçoit le nombre de sous-clés contenues dans la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="30dd9-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="30dd9-122">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-123">*lpcMaxSubKeyLen* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-124">Pointeur vers une variable qui reçoit la taille de la sous-clé de la clé avec le nom le plus long, en caractères Unicode, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="30dd9-125">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-126">*lpcMaxClassLen* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-127">Pointeur vers une variable qui reçoit la taille de la chaîne la plus longue qui spécifie une classe de sous-clé, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dd9-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="30dd9-128">Le nombre retourné n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="30dd9-129">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-130">*lpcValues* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-131">Pointeur vers une variable qui reçoit le nombre de valeurs associées à la clé.</span><span class="sxs-lookup"><span data-stu-id="30dd9-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="30dd9-132">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-133">*lpcMaxValueNameLen* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-134">Pointeur vers une variable qui reçoit la taille du nom de la valeur la plus longue de la clé, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="30dd9-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="30dd9-135">La taille n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="30dd9-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="30dd9-136">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-137">*lpcMaxValueLen* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-138">Pointeur vers une variable qui reçoit la taille du composant de données le plus long parmi les valeurs de la clé, en octets.</span><span class="sxs-lookup"><span data-stu-id="30dd9-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="30dd9-139">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-140">*lpcbSecurityDescriptor* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-141">Pointeur vers une variable qui reçoit la taille du descripteur de sécurité de la clé, en octets.</span><span class="sxs-lookup"><span data-stu-id="30dd9-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="30dd9-142">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30dd9-143">*lpftLastWriteTime* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30dd9-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30dd9-144">Pointeur vers une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui reçoit l’heure de la dernière écriture.</span><span class="sxs-lookup"><span data-stu-id="30dd9-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="30dd9-145">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="30dd9-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="30dd9-146">La fonction définit les membres de la structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) pour indiquer l’heure de la dernière modification de la clé ou de l’une de ses entrées de valeur.</span><span class="sxs-lookup"><span data-stu-id="30dd9-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30dd9-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30dd9-147">Return value</span></span>

<span data-ttu-id="30dd9-148">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="30dd9-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="30dd9-149">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="30dd9-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="30dd9-150">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="30dd9-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="30dd9-151">Si la mémoire tampon *lpClass* est trop petite pour recevoir le nom de la classe, la fonction retourne l’erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="30dd9-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="30dd9-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30dd9-152">Requirements</span></span>



| <span data-ttu-id="30dd9-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30dd9-153">Requirement</span></span> | <span data-ttu-id="30dd9-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="30dd9-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30dd9-155">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="30dd9-155">Redistributable</span></span><br/> | <span data-ttu-id="30dd9-156">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="30dd9-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="30dd9-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="30dd9-157">Header</span></span><br/>          | <dl> <span data-ttu-id="30dd9-158"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="30dd9-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="30dd9-159">DLL</span><span class="sxs-lookup"><span data-stu-id="30dd9-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="30dd9-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30dd9-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30dd9-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30dd9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dd9-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="30dd9-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="30dd9-163">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="30dd9-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="30dd9-164">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="30dd9-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="30dd9-165">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="30dd9-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
