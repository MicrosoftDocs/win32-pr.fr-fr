---
description: La fonction EnumPrinterDrivers énumère les pilotes d’imprimante installés sur un serveur d’impression spécifié.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: EnumPrinterDrivers, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756394"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="6e48a-103">EnumPrinterDrivers fonction)</span><span class="sxs-lookup"><span data-stu-id="6e48a-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="6e48a-104">La fonction **EnumPrinterDrivers** énumère les pilotes d’imprimante installés sur un serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e48a-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e48a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e48a-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="6e48a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e48a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e48a-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel les pilotes d’imprimante sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="6e48a-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="6e48a-109">Si *pname* a la **valeur null**, la fonction énumère les pilotes d’imprimante locaux.</span><span class="sxs-lookup"><span data-stu-id="6e48a-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="6e48a-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64, Windows x64 ou Windows NT R4000).</span><span class="sxs-lookup"><span data-stu-id="6e48a-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="6e48a-112">Si ce paramètre a la **valeur null**, la fonction utilise l’environnement actuel de l’appelant/client (pas du serveur/de destination).</span><span class="sxs-lookup"><span data-stu-id="6e48a-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="6e48a-113">Si la chaîne *pEnvironment* spécifie « All », **EnumPrinterDrivers** énumère les pilotes d’imprimante pour toutes les plateformes installées sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e48a-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="6e48a-114">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-115">Type de structure d’informations retourné dans la mémoire tampon *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="6e48a-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="6e48a-116">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6e48a-116">It can be one of the following.</span></span>



| <span data-ttu-id="6e48a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e48a-117">Value</span></span>                                                                                                | <span data-ttu-id="6e48a-118">Signification</span><span class="sxs-lookup"><span data-stu-id="6e48a-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="6e48a-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-120">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6e48a-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="6e48a-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-122">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e48a-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="6e48a-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-124">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6e48a-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="6e48a-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-126">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="6e48a-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="6e48a-127"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-128">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="6e48a-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="6e48a-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-130">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="6e48a-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="6e48a-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="6e48a-132">**\_Informations sur le pilote \_ 8**</span><span class="sxs-lookup"><span data-stu-id="6e48a-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="6e48a-133">*pDriverInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-134">Pointeur vers une mémoire tampon qui reçoit un tableau de structures d’informations de pilotes \_ \_ \* , tel que spécifié par le *niveau*.</span><span class="sxs-lookup"><span data-stu-id="6e48a-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="6e48a-135">Chaque structure contient des données qui décrivent un pilote d’imprimante disponible.</span><span class="sxs-lookup"><span data-stu-id="6e48a-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="6e48a-136">La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="6e48a-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="6e48a-137">Pour déterminer la taille de mémoire tampon requise, appelez **EnumPrinterDrivers** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="6e48a-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="6e48a-138">**EnumPrinterDrivers** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="6e48a-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="6e48a-139">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-140">Taille, en octets, de la mémoire tampon vers laquelle pointe *pDriverInfo*</span><span class="sxs-lookup"><span data-stu-id="6e48a-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="6e48a-141">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-142">Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pDriverInfo* si la fonction est réussie.</span><span class="sxs-lookup"><span data-stu-id="6e48a-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="6e48a-143">Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="6e48a-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="6e48a-144">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e48a-145">Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="6e48a-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="6e48a-146">Il s’agit du nombre de pilotes d’imprimante installés sur le serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e48a-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e48a-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e48a-147">Return value</span></span>

<span data-ttu-id="6e48a-148">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6e48a-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6e48a-149">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6e48a-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e48a-150">Notes</span><span class="sxs-lookup"><span data-stu-id="6e48a-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e48a-151">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6e48a-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6e48a-152">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="6e48a-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6e48a-153">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="6e48a-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e48a-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e48a-154">Requirements</span></span>



| <span data-ttu-id="6e48a-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e48a-155">Requirement</span></span> | <span data-ttu-id="6e48a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e48a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e48a-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e48a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6e48a-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6e48a-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e48a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6e48a-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e48a-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6e48a-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e48a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e48a-162"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6e48a-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e48a-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e48a-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6e48a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="6e48a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e48a-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6e48a-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6e48a-167">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6e48a-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6e48a-168">**EnumPrinterDriversW** (Unicode) et **EnumPrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6e48a-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="6e48a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e48a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e48a-170">Impression</span><span class="sxs-lookup"><span data-stu-id="6e48a-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6e48a-171">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="6e48a-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6e48a-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="6e48a-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="6e48a-173">**\_Informations sur le pilote \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6e48a-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="6e48a-174">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e48a-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="6e48a-175">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6e48a-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="6e48a-176">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="6e48a-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="6e48a-177">**\_Informations sur le pilote \_ 5**</span><span class="sxs-lookup"><span data-stu-id="6e48a-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="6e48a-178">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="6e48a-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="6e48a-179">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="6e48a-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

