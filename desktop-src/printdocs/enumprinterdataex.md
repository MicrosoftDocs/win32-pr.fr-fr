---
description: La fonction EnumPrinterDataEx énumère tous les noms de valeur et les données pour une imprimante et une clé spécifiées.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: EnumPrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757852"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="411f6-103">EnumPrinterDataEx fonction)</span><span class="sxs-lookup"><span data-stu-id="411f6-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="411f6-104">La fonction **EnumPrinterDataEx** énumère tous les noms de valeur et les données pour une imprimante et une clé spécifiées.</span><span class="sxs-lookup"><span data-stu-id="411f6-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="411f6-105">Les données de l’imprimante sont stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="411f6-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="411f6-106">Lors de l’énumération des données d’imprimante, n’appelez pas les fonctions de Registre susceptibles de modifier les données.</span><span class="sxs-lookup"><span data-stu-id="411f6-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="411f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="411f6-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="411f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="411f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411f6-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="411f6-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-110">Handle vers l’imprimante pour laquelle la fonction récupère les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="411f6-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="411f6-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="411f6-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="411f6-112">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="411f6-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant les valeurs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="411f6-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="411f6-114">Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès avec une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="411f6-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="411f6-115">**EnumPrinterDataEx** énumère toutes les valeurs de la clé, mais n’énumère pas les valeurs des sous-clés de la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="411f6-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="411f6-116">Utilisez la fonction [**EnumPrinterKey**](enumprinterkey.md) pour énumérer les sous-clés.</span><span class="sxs-lookup"><span data-stu-id="411f6-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="411f6-117">Si *pKeyName* a la **valeur null** ou est une chaîne vide, **ENUMPRINTERDATAEX** retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="411f6-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="411f6-118">*pEnumValues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="411f6-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-119">Pointeur vers une mémoire tampon qui reçoit un tableau de structures de [**\_ \_ valeurs d’enum d’imprimante**](printer-enum-values.md) .</span><span class="sxs-lookup"><span data-stu-id="411f6-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="411f6-120">Chaque structure contient le nom de la valeur, le type, les données et la taille d’une valeur sous la clé.</span><span class="sxs-lookup"><span data-stu-id="411f6-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="411f6-121">*cbEnumValues* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="411f6-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-122">Taille, en octets, de la mémoire tampon vers laquelle pointe *pcbEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="411f6-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="411f6-123">Si vous affectez à *cbEnumValues* la valeur zéro, le paramètre *pcbEnumValues* retourne la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="411f6-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="411f6-124">*pcbEnumValues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="411f6-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-125">Pointeur vers une variable qui reçoit la taille, en octets, des données de configuration récupérées.</span><span class="sxs-lookup"><span data-stu-id="411f6-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="411f6-126">Si la taille de la mémoire tampon spécifiée par *cbEnumValues* est trop petite, la fonction retourne \_ l’erreur plus \_ de données et *pcbEnumValues* indique la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="411f6-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="411f6-127">*pnEnumValues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="411f6-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411f6-128">Pointeur vers une variable qui reçoit le nombre de structures [**de \_ \_ valeurs d’enum d’imprimante**](printer-enum-values.md) retournées dans *pEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="411f6-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="411f6-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="411f6-129">Return value</span></span>

<span data-ttu-id="411f6-130">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="411f6-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="411f6-131">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="411f6-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="411f6-132">Notes</span><span class="sxs-lookup"><span data-stu-id="411f6-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="411f6-133">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="411f6-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="411f6-134">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="411f6-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="411f6-135">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="411f6-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="411f6-136">**EnumPrinterDataEx** récupère les données de configuration de l’imprimante définies par les fonctions [**SetPrinterDataEx**](setprinterdataex.md) et [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="411f6-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="411f6-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="411f6-137">Requirements</span></span>



| <span data-ttu-id="411f6-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="411f6-138">Requirement</span></span> | <span data-ttu-id="411f6-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="411f6-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="411f6-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411f6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="411f6-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="411f6-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="411f6-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="411f6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="411f6-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="411f6-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="411f6-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="411f6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="411f6-145"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="411f6-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="411f6-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="411f6-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="411f6-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="411f6-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="411f6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="411f6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411f6-149"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="411f6-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="411f6-150">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="411f6-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="411f6-151">**EnumPrinterDataExW** (Unicode) et **EnumPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="411f6-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="411f6-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="411f6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411f6-153">Impression</span><span class="sxs-lookup"><span data-stu-id="411f6-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="411f6-154">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="411f6-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="411f6-155">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="411f6-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="411f6-156">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="411f6-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="411f6-157">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="411f6-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="411f6-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="411f6-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="411f6-159">**\_valeurs d’énumération d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="411f6-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="411f6-160">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="411f6-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="411f6-161">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="411f6-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




