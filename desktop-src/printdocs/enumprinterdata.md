---
description: La fonction EnumPrinterData énumère les données de configuration d’une imprimante spécifiée.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: EnumPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202693"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="f8dd4-103">EnumPrinterData fonction)</span><span class="sxs-lookup"><span data-stu-id="f8dd4-103">EnumPrinterData function</span></span>

<span data-ttu-id="f8dd4-104">La fonction **EnumPrinterData** énumère les données de configuration d’une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="f8dd4-105">Pour récupérer les données de configuration en un seul appel, utilisez la fonction [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="f8dd4-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8dd4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8dd4-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="f8dd4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8dd4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8dd4-108">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-109">Handle vers l’imprimante dont les données de configuration doivent être obtenues.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="f8dd4-110">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-111">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-112">Valeur d’index qui spécifie la valeur des données de configuration à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="f8dd4-113">Affectez à ce paramètre la valeur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="f8dd4-114">Incrémentez ensuite le paramètre d’une unité pour les appels suivants impliquant la même imprimante, jusqu’à ce que la fonction retourne l’erreur \_ \_ plus d' \_ éléments.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="f8dd4-115">Pour plus d’informations, consultez la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="f8dd4-116">Si vous utilisez la technique mentionnée dans les descriptions des paramètres *cbValueName* et *cbData* pour obtenir les valeurs de taille de mémoire tampon adéquates, en définissant ces deux paramètres sur zéro dans un premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié, la valeur de *dwIndex* n’a pas d’importance pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="f8dd4-117">Affectez à *dwIndex* la valeur zéro dans le prochain appel à **EnumPrinterData** pour démarrer le processus d’énumération réel.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="f8dd4-118">Les valeurs des données de configuration ne sont pas triées.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="f8dd4-119">Les nouvelles valeurs comporteront un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="f8dd4-120">Cela signifie que la fonction **EnumPrinterData** peut retourner des valeurs dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-121">*pValueName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-122">Pointeur vers une mémoire tampon qui reçoit le nom de la valeur des données de configuration, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-123">*cbValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-124">Taille, en octets, de la mémoire tampon vers laquelle pointe *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="f8dd4-125">Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, définissez à la fois ce paramètre et le paramètre *cbData* sur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="f8dd4-126">Quand la fonction retourne, la variable vers laquelle pointe *pcbValueName* contient une taille de mémoire tampon suffisamment grande pour énumérer correctement tous les noms de valeur de données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-127">*pcbValueName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-128">Pointeur vers une variable qui reçoit le nombre d’octets stockés dans la mémoire tampon vers laquelle pointe *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-129">*PTYPE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-130">Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="f8dd4-131">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="f8dd4-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="f8dd4-132">Le paramètre *PTYPE* peut avoir la **valeur null** si le code de type n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-133">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-134">Pointeur vers une mémoire tampon qui reçoit la valeur des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="f8dd4-135">Ce paramètre peut avoir la valeur **null** si la valeur des données de configuration n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-136">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-137">Taille, en octets, de la mémoire tampon vers laquelle pointe *pData*.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="f8dd4-138">Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, définissez à la fois ce paramètre et le paramètre *cbValueName* sur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="f8dd4-139">Quand la fonction retourne, la variable vers laquelle pointe *pcbData* contient une taille de mémoire tampon suffisamment grande pour énumérer correctement tous les noms de valeur de données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="f8dd4-140">*pcbData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dd4-141">Pointeur vers une variable qui reçoit le nombre d’octets stockés dans la mémoire tampon vers laquelle pointe *pData*.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="f8dd4-142">Ce paramètre peut avoir la **valeur null** si *PData* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8dd4-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8dd4-143">Return value</span></span>

<span data-ttu-id="f8dd4-144">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f8dd4-145">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="f8dd4-146">La fonction retourne l’erreur \_ aucun \_ autre \_ élément lorsqu’il n’y a plus de valeurs de données de configuration à récupérer pour un handle d’imprimante spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8dd4-147">Notes</span><span class="sxs-lookup"><span data-stu-id="f8dd4-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8dd4-148">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f8dd4-149">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f8dd4-150">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f8dd4-151">**EnumPrinterData** récupère les données de configuration de l’imprimante définies par la fonction [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f8dd4-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="f8dd4-152">Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="f8dd4-153">La fonction **EnumPrinterData** obtient l’une de ces valeurs, son nom et un code de type, chaque fois que vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="f8dd4-154">Appelez la fonction **EnumPrinterData** plusieurs fois de suite pour obtenir toutes les valeurs de données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="f8dd4-155">Les données de configuration de l’imprimante sont stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="f8dd4-156">Lors de l’énumération des données de configuration de l’imprimante, vous devez éviter d’appeler des fonctions de Registre susceptibles de modifier ces données.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="f8dd4-157">Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, appelez d’abord **EnumPrinterData** avec les paramètres *cbValueName* et *cbData* définis sur zéro, comme indiqué plus haut dans la section paramètres.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="f8dd4-158">La valeur de *dwIndex* n’a pas d’importance pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="f8dd4-159">Quand la fonction retourne, \* *pcbValueName* et \* *pcbData* contiendront des tailles de mémoire tampon suffisamment grandes pour énumérer tous les noms et valeurs de la valeur des données de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="f8dd4-160">Lors du prochain appel, allouez un nom de valeur et des mémoires tampons de données, définissez *cbValueName* et *cbData* sur les tailles en octets des mémoires tampons allouées, puis définissez *dwIndex* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="f8dd4-161">Ensuite, continuez à appeler la fonction **EnumPrinterData** , en incrémentant *dwIndex* à chaque fois, jusqu’à ce que la fonction retourne l’erreur plus \_ aucun \_ \_ élément.</span><span class="sxs-lookup"><span data-stu-id="f8dd4-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dd4-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8dd4-162">Requirements</span></span>



| <span data-ttu-id="f8dd4-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8dd4-163">Requirement</span></span> | <span data-ttu-id="f8dd4-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8dd4-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dd4-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8dd4-165">Minimum supported client</span></span><br/> | <span data-ttu-id="f8dd4-166">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8dd4-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8dd4-167">Minimum supported server</span></span><br/> | <span data-ttu-id="f8dd4-168">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8dd4-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8dd4-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8dd4-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8dd4-170"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8dd4-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8dd4-171">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8dd4-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8dd4-172"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8dd4-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f8dd4-173">DLL</span><span class="sxs-lookup"><span data-stu-id="f8dd4-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8dd4-174"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f8dd4-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f8dd4-175">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f8dd4-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8dd4-176">**EnumPrinterDataW** (Unicode) et **EnumPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8dd4-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="f8dd4-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8dd4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dd4-178">Impression</span><span class="sxs-lookup"><span data-stu-id="f8dd4-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-179">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f8dd4-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-180">**DeletePrinterData**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-181">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-182">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-184">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f8dd4-185">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="f8dd4-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

