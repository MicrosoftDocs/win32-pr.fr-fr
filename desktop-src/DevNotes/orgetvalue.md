---
description: Récupère le type et les données pour la valeur de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: ORGetValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541128"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="b1bc3-103">ORGetValue fonction)</span><span class="sxs-lookup"><span data-stu-id="b1bc3-103">ORGetValue function</span></span>

<span data-ttu-id="b1bc3-104">Récupère le type et les données pour la valeur de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1bc3-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="b1bc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1bc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bc3-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc3-109">*lpSubKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-110">Nom de la clé de Registre.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-110">The name of the registry key.</span></span> <span data-ttu-id="b1bc3-111">Cette clé doit être une sous-clé de la clé spécifiée par le paramètre *handle* .</span><span class="sxs-lookup"><span data-stu-id="b1bc3-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="b1bc3-112">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="b1bc3-113">Les noms de clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc3-114">*lpValue* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-115">Nom de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-115">The name of the registry value.</span></span> <span data-ttu-id="b1bc3-116">Si ce paramètre a la valeur **null** ou est une chaîne vide, "", la fonction récupère le type et les données pour la valeur sans nom ou par défaut de la clé, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="b1bc3-117">Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="b1bc3-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="b1bc3-118">Les clés n’ont pas automatiquement une valeur sans nom ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="b1bc3-119">Les valeurs sans nom peuvent être de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="b1bc3-120">Les noms de valeurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc3-121">*pdwType* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-122">Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="b1bc3-123">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="b1bc3-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="b1bc3-124">Ce paramètre peut avoir la **valeur null** si le type n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc3-125">*pvData* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-126">Pointeur vers une mémoire tampon qui reçoit les données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="b1bc3-127">Ce paramètre peut avoir la **valeur null** si les données ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="b1bc3-128">Si les données sont une chaîne, la fonction recherche un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="b1bc3-129">Si aucun n’est trouvé, la chaîne est stockée avec une marque de fin null si la mémoire tampon est suffisamment grande pour contenir le caractère supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="b1bc3-130">Dans le cas contraire, la fonction échoue et retourne une erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc3-131">*pcbData* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b1bc3-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bc3-132">Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *pvData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="b1bc3-133">Quand la fonction retourne une valeur, cette variable contient la taille des données copiées dans *pvData*.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="b1bc3-134">Le paramètre *pcbData* peut être **null** uniquement si *pvData* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="b1bc3-135">Si les données ont le \_ type reg SZ, \_ reg \_ multisz ou reg \_ expand \_ SZ, cette taille inclut tous les caractères null de fin.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="b1bc3-136">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-136">For more information, see Remarks.</span></span>

<span data-ttu-id="b1bc3-137">Si la mémoire tampon spécifiée par le paramètre *pvData* n’est pas assez grande pour contenir les données, la fonction retourne l’erreur \_ plus de \_ données et stocke la taille de mémoire tampon requise dans la variable vers laquelle pointe *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="b1bc3-138">Dans ce cas, le contenu de la mémoire tampon *pvData* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="b1bc3-139">Si *pvData* a la **valeur null** et que *PcbData* n’a pas la **valeur null**, la fonction retourne \_ la réussite de l’erreur et stocke la taille des données, en octets, dans la variable vers laquelle pointe *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="b1bc3-140">Cela permet à une application de déterminer la meilleure façon d’allouer une mémoire tampon pour les données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bc3-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1bc3-141">Return value</span></span>

<span data-ttu-id="b1bc3-142">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b1bc3-143">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="b1bc3-144">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1bc3-145">Notes</span><span class="sxs-lookup"><span data-stu-id="b1bc3-145">Remarks</span></span>

<span data-ttu-id="b1bc3-146">Une application appelle généralement la fonction [**OREnumValue**](orenumvalue.md) pour déterminer les noms de valeur, puis appelle la fonction **ORGetValue** pour récupérer les données pour les noms.</span><span class="sxs-lookup"><span data-stu-id="b1bc3-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bc3-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1bc3-147">Requirements</span></span>



| <span data-ttu-id="b1bc3-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1bc3-148">Requirement</span></span> | <span data-ttu-id="b1bc3-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1bc3-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bc3-150">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b1bc3-150">Redistributable</span></span><br/> | <span data-ttu-id="b1bc3-151">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b1bc3-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="b1bc3-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1bc3-152">Header</span></span><br/>          | <dl> <span data-ttu-id="b1bc3-153"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bc3-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1bc3-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bc3-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="b1bc3-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1bc3-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bc3-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1bc3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bc3-157">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="b1bc3-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="b1bc3-158">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="b1bc3-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="b1bc3-159">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="b1bc3-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="b1bc3-160">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="b1bc3-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="b1bc3-161">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="b1bc3-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
