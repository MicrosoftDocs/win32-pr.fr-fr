---
description: Énumère les sous-clés de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations sur une sous-clé chaque fois qu’elle est appelée.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: OREnumKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540592"
---
# <a name="orenumkey-function"></a><span data-ttu-id="7cd60-104">OREnumKey fonction)</span><span class="sxs-lookup"><span data-stu-id="7cd60-104">OREnumKey function</span></span>

<span data-ttu-id="7cd60-105">Énumère les sous-clés de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7cd60-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="7cd60-106">La fonction récupère des informations sur une sous-clé chaque fois qu’elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="7cd60-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd60-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd60-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="7cd60-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cd60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd60-109">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-110">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7cd60-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-111">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-112">Index de la sous-clé à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7cd60-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="7cd60-113">Ce paramètre doit avoir la valeur zéro pour le premier appel à la fonction, puis être incrémenté pour les appels suivants.</span><span class="sxs-lookup"><span data-stu-id="7cd60-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="7cd60-114">Comme les sous-clés ne sont pas triées, toute nouvelle sous-clé aura un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7cd60-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="7cd60-115">Cela signifie que la fonction peut retourner des sous-clés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="7cd60-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-116">*lpName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-117">Pointeur vers une mémoire tampon qui reçoit le nom de la sous-clé, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7cd60-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="7cd60-118">La fonction copie uniquement le nom de la sous-clé, et non la hiérarchie de clé complète, dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7cd60-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="7cd60-119">Si la fonction échoue, aucune information n’est copiée dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7cd60-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="7cd60-120">Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="7cd60-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-121">*lpcName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-122">Pointeur vers une variable qui spécifie la taille de la mémoire tampon spécifiée par le paramètre *lpName* , dans **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="7cd60-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="7cd60-123">Cette taille doit inclure le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7cd60-123">This size should include the terminating null character.</span></span> <span data-ttu-id="7cd60-124">Si la fonction est réussie, la variable vers laquelle pointe *lpcName* contient le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7cd60-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-125">*lpClass* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-126">Pointeur vers une mémoire tampon qui reçoit la chaîne de classe terminée par le caractère null de la sous-clé énumérée.</span><span class="sxs-lookup"><span data-stu-id="7cd60-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="7cd60-127">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7cd60-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-128">*lpcClass* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-129">Pointeur vers une variable qui spécifie la taille de la mémoire tampon spécifiée par le paramètre *lpClass* , dans **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="7cd60-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="7cd60-130">La taille doit inclure le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7cd60-130">The size should include the terminating null character.</span></span> <span data-ttu-id="7cd60-131">Si la fonction est réussie, *lpcClass* contient le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7cd60-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="7cd60-132">Ce paramètre peut être **null** uniquement si *LpClass* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7cd60-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd60-133">*lpftLastWriteTime* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7cd60-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd60-134">Pointeur vers une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui reçoit l’heure de la dernière écriture dans la sous-clé énumérée.</span><span class="sxs-lookup"><span data-stu-id="7cd60-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="7cd60-135">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7cd60-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd60-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cd60-136">Return value</span></span>

<span data-ttu-id="7cd60-137">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="7cd60-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7cd60-138">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="7cd60-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="7cd60-139">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7cd60-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="7cd60-140">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7cd60-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="7cd60-141">Si la mémoire tampon *lpName* est trop petite pour recevoir le nom de la clé, la fonction retourne l’erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="7cd60-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="7cd60-142">S’il n’y a plus de sous-clés disponibles, la fonction retourne l’erreur plus \_ aucun \_ \_ élément.</span><span class="sxs-lookup"><span data-stu-id="7cd60-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd60-143">Notes</span><span class="sxs-lookup"><span data-stu-id="7cd60-143">Remarks</span></span>

<span data-ttu-id="7cd60-144">Pour énumérer les sous-clés, une application doit appeler initialement la fonction **OREnumKey** avec le paramètre *dwIndex* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="7cd60-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="7cd60-145">L’application doit ensuite incrémenter le paramètre *dwIndex* et appeler **OREnumKey** jusqu’à ce qu’il n’y ait plus de sous-clés (ce qui signifie que la fonction retourne l’erreur \_ aucun \_ autre \_ élément).</span><span class="sxs-lookup"><span data-stu-id="7cd60-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="7cd60-146">L’application peut également définir *dwIndex* sur l’index de la dernière sous-clé sur le premier appel à la fonction et décrémenter l’index jusqu’à ce que la sous-clé avec l’index 0 soit énumérée.</span><span class="sxs-lookup"><span data-stu-id="7cd60-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="7cd60-147">Pour récupérer l’index de la dernière sous-clé, utilisez la fonction [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .</span><span class="sxs-lookup"><span data-stu-id="7cd60-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="7cd60-148">Lorsqu’une application utilise la fonction **OREnumKey** , elle ne doit pas effectuer d’appels à des fonctions de Registre hors connexion qui peuvent modifier la clé énumérée.</span><span class="sxs-lookup"><span data-stu-id="7cd60-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd60-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd60-149">Requirements</span></span>



| <span data-ttu-id="7cd60-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd60-150">Requirement</span></span> | <span data-ttu-id="7cd60-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd60-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd60-152">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7cd60-152">Redistributable</span></span><br/> | <span data-ttu-id="7cd60-153">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7cd60-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="7cd60-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cd60-154">Header</span></span><br/>          | <dl> <span data-ttu-id="7cd60-155"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd60-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cd60-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd60-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="7cd60-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd60-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd60-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd60-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd60-159">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="7cd60-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="7cd60-160">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="7cd60-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="7cd60-161">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="7cd60-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="7cd60-162">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="7cd60-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
