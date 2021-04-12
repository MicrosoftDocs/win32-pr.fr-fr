---
description: La fonction EnumPrinterKey énumère les sous-clés d’une clé spécifiée pour une imprimante spécifiée.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: EnumPrinterKey, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319974"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="f977b-103">EnumPrinterKey fonction)</span><span class="sxs-lookup"><span data-stu-id="f977b-103">EnumPrinterKey function</span></span>

<span data-ttu-id="f977b-104">La fonction **EnumPrinterKey** énumère les sous-clés d’une clé spécifiée pour une imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f977b-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="f977b-105">Les données de l’imprimante sont stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f977b-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="f977b-106">Lors de l’énumération des données d’imprimante, n’appelez pas les fonctions de Registre susceptibles de modifier les données.</span><span class="sxs-lookup"><span data-stu-id="f977b-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f977b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f977b-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="f977b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f977b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f977b-109">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f977b-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f977b-110">Handle vers l’imprimante pour laquelle la fonction énumère les sous-clés.</span><span class="sxs-lookup"><span data-stu-id="f977b-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="f977b-111">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f977b-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f977b-112">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f977b-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f977b-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant les sous-clés à énumérer.</span><span class="sxs-lookup"><span data-stu-id="f977b-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="f977b-114">Utilisez la barre oblique inverse « \\ » comme séparateur pour spécifier un chemin d’accès avec une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="f977b-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="f977b-115">**EnumPrinterKey** énumère toutes les sous-clés de la clé, mais n’énumère pas les sous-clés de ces sous-clés.</span><span class="sxs-lookup"><span data-stu-id="f977b-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="f977b-116">Si *pKeyName* est une chaîne vide (""), **EnumPrinterKey** énumère la clé de niveau supérieur pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f977b-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="f977b-117">Si *pKeyName* a la **valeur null**, **ENUMPRINTERKEY** retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="f977b-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="f977b-118">*pSubkey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f977b-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f977b-119">Pointeur vers une mémoire tampon qui reçoit un tableau de noms de sous-clés se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="f977b-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="f977b-120">Le tableau se termine par deux caractères null.</span><span class="sxs-lookup"><span data-stu-id="f977b-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="f977b-121">*cbSubkey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f977b-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f977b-122">Taille, en octets, de la mémoire tampon vers laquelle pointe *pSubkey*.</span><span class="sxs-lookup"><span data-stu-id="f977b-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="f977b-123">Si vous affectez à *cbSubkey* la valeur zéro, le paramètre *pcbSubkey* retourne la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="f977b-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="f977b-124">*pcbSubkey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f977b-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f977b-125">Pointeur vers une variable qui reçoit le nombre d’octets récupérés dans la mémoire tampon *pSubkey* .</span><span class="sxs-lookup"><span data-stu-id="f977b-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="f977b-126">Si la taille de la mémoire tampon spécifiée par *cbSubkey* est trop petite, la fonction retourne \_ l’erreur plus \_ de données et *pcbSubkey* indique la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="f977b-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f977b-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f977b-127">Return value</span></span>

<span data-ttu-id="f977b-128">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="f977b-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f977b-129">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="f977b-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="f977b-130">Si *pKeyName* n’existe pas, la valeur de retour est \_ fichier d’erreurs \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="f977b-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="f977b-131">Notes</span><span class="sxs-lookup"><span data-stu-id="f977b-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f977b-132">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f977b-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f977b-133">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="f977b-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f977b-134">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="f977b-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f977b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f977b-135">Requirements</span></span>



| <span data-ttu-id="f977b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f977b-136">Requirement</span></span> | <span data-ttu-id="f977b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f977b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f977b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f977b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f977b-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f977b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f977b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f977b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f977b-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f977b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f977b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="f977b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f977b-143"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f977b-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f977b-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f977b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="f977b-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f977b-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f977b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f977b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f977b-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f977b-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f977b-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f977b-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f977b-149">**EnumPrinterKeyW** (Unicode) et **EnumPrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f977b-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="f977b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f977b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f977b-151">Impression</span><span class="sxs-lookup"><span data-stu-id="f977b-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f977b-152">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f977b-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f977b-153">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f977b-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f977b-154">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f977b-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f977b-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f977b-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f977b-156">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f977b-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




