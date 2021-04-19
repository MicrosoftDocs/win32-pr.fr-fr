---
description: Énumère les valeurs de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations pour une valeur sous la clé spécifiée chaque fois que la fonction est appelée.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: OREnumValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524028"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="06476-104">OREnumValue fonction)</span><span class="sxs-lookup"><span data-stu-id="06476-104">OREnumValue function</span></span>

<span data-ttu-id="06476-105">Énumère les valeurs de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="06476-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="06476-106">La fonction récupère des informations pour une valeur sous la clé spécifiée chaque fois que la fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="06476-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="06476-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06476-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="06476-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06476-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06476-109">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06476-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-110">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="06476-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="06476-111">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06476-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-112">Index de la valeur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="06476-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="06476-113">Ce paramètre doit être égal à zéro pour le premier appel à la fonction, puis être incrémenté pour les appels suivants.</span><span class="sxs-lookup"><span data-stu-id="06476-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="06476-114">Étant donné que les valeurs ne sont pas triées, toute nouvelle valeur aura un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="06476-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="06476-115">Cela signifie que la fonction peut retourner des valeurs dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="06476-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="06476-116">*lpValueName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06476-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-117">Pointeur vers une mémoire tampon qui reçoit le nom de la valeur sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="06476-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="06476-118">Cette mémoire tampon doit être suffisamment grande pour inclure le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="06476-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="06476-119">Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="06476-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="06476-120">*lpcValueName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06476-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-121">Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpValueName* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="06476-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="06476-122">Quand la fonction retourne, la variable reçoit le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="06476-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="06476-123">*lpType* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06476-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-124">Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="06476-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="06476-125">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="06476-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="06476-126">Le paramètre *lpType* peut avoir la **valeur null** si le code de type n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="06476-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="06476-127">*lpData* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06476-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-128">Pointeur vers une mémoire tampon qui reçoit les données de l’entrée de valeur.</span><span class="sxs-lookup"><span data-stu-id="06476-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="06476-129">Ce paramètre peut avoir la **valeur null** si les données ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="06476-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="06476-130">Si *lpData* a la **valeur null** et que *LpcbData* n’a pas la **valeur null**, la fonction stocke la taille des données, en octets, dans la variable vers laquelle pointe *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="06476-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="06476-131">Cela permet à une application de déterminer la meilleure façon d’allouer une mémoire tampon pour les données.</span><span class="sxs-lookup"><span data-stu-id="06476-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="06476-132">*lpcbData* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06476-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06476-133">Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="06476-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="06476-134">Lorsque la fonction retourne, la variable reçoit le nombre d’octets stockés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06476-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="06476-135">Ce paramètre peut être **null** uniquement si *LpData* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="06476-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="06476-136">Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, cette taille inclut tous les caractères null de fin.</span><span class="sxs-lookup"><span data-stu-id="06476-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="06476-137">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="06476-137">For more information, see Remarks.</span></span>

<span data-ttu-id="06476-138">Si la mémoire tampon spécifiée par *lpData* n’est pas suffisamment grande pour contenir les données, la fonction retourne l’erreur \_ plus de \_ données et stocke la taille de mémoire tampon requise dans la variable vers laquelle pointe *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="06476-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="06476-139">Dans ce cas, le contenu de *lpData* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="06476-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06476-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06476-140">Return value</span></span>

<span data-ttu-id="06476-141">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="06476-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="06476-142">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="06476-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="06476-143">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="06476-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="06476-144">Si la mémoire tampon *lpData* est trop petite pour recevoir la valeur, la fonction retourne l’erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="06476-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="06476-145">Notes</span><span class="sxs-lookup"><span data-stu-id="06476-145">Remarks</span></span>

<span data-ttu-id="06476-146">Pour énumérer des valeurs, une application doit appeler initialement la fonction **OREnumValue** avec le paramètre *dwIndex* défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="06476-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="06476-147">L’application doit ensuite incrémenter *dwIndex* et appeler la fonction **OREnumValue** jusqu’à ce qu’il n’y ait plus de valeur (jusqu’à ce que la fonction retourne l’erreur plus \_ aucun \_ \_ élément).</span><span class="sxs-lookup"><span data-stu-id="06476-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="06476-148">L’application peut également définir *dwIndex* sur l’index de la dernière valeur sur le premier appel à la fonction et décrémenter l’index jusqu’à ce que la valeur avec l’index 0 soit énumérée.</span><span class="sxs-lookup"><span data-stu-id="06476-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="06476-149">Pour récupérer l’index de la dernière valeur, utilisez la fonction [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="06476-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="06476-150">Lors de l’utilisation de **OREnumValue**, une application ne doit pas appeler de fonctions de Registre hors connexion qui peuvent modifier la clé en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="06476-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="06476-151">Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, la chaîne n’a peut-être pas été stockée avec les caractères de fin null corrects.</span><span class="sxs-lookup"><span data-stu-id="06476-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="06476-152">Par conséquent, même si la fonction retourne \_ une erreur, l’application doit s’assurer que la chaîne se termine correctement avant de l’utiliser ; sinon, elle peut remplacer une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06476-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="06476-153">(Notez que REG \_ \_Les chaînes à plusieurs SZ doivent avoir deux caractères de fin null.)</span><span class="sxs-lookup"><span data-stu-id="06476-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="06476-154">Pour déterminer la taille maximale du nom et des tampons de données, utilisez la fonction [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="06476-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06476-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06476-155">Requirements</span></span>



| <span data-ttu-id="06476-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06476-156">Requirement</span></span> | <span data-ttu-id="06476-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="06476-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06476-158">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="06476-158">Redistributable</span></span><br/> | <span data-ttu-id="06476-159">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="06476-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="06476-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="06476-160">Header</span></span><br/>          | <dl> <span data-ttu-id="06476-161"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="06476-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="06476-162">DLL</span><span class="sxs-lookup"><span data-stu-id="06476-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="06476-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06476-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06476-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06476-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06476-165">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="06476-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="06476-166">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="06476-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="06476-167">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="06476-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="06476-168">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="06476-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
