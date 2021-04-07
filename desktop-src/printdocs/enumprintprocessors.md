---
description: La fonction EnumPrintProcessors énumère les processeurs d’impression installés sur le serveur spécifié.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: EnumPrintProcessors, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952337"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="71c15-103">EnumPrintProcessors fonction)</span><span class="sxs-lookup"><span data-stu-id="71c15-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="71c15-104">La fonction **EnumPrintProcessors** énumère les processeurs d’impression installés sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="71c15-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71c15-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="71c15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71c15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c15-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71c15-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel résident les processeurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="71c15-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="71c15-109">Si ce paramètre a la **valeur null**, les processeurs d’impression locaux sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="71c15-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71c15-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="71c15-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="71c15-112">Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="71c15-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71c15-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-114">Type d’informations retournées dans la mémoire tampon *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="71c15-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="71c15-115">Ce paramètre doit être 1.</span><span class="sxs-lookup"><span data-stu-id="71c15-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-116">*pPrintProcessorInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71c15-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-117">Pointeur vers une mémoire tampon qui reçoit un tableau de structures [**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="71c15-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="71c15-118">Chaque structure décrit un processeur d’impression disponible.</span><span class="sxs-lookup"><span data-stu-id="71c15-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="71c15-119">La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="71c15-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="71c15-120">Pour déterminer la taille de mémoire tampon requise, appelez **EnumPrintProcessors** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="71c15-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="71c15-121">**EnumPrintProcessors** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="71c15-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-122">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71c15-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-123">Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="71c15-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-124">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71c15-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-125">Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pPrintProcessorInfo* si la fonction est réussie.</span><span class="sxs-lookup"><span data-stu-id="71c15-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="71c15-126">Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="71c15-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="71c15-127">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71c15-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71c15-128">Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="71c15-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c15-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71c15-129">Return value</span></span>

<span data-ttu-id="71c15-130">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="71c15-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="71c15-131">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="71c15-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c15-132">Notes</span><span class="sxs-lookup"><span data-stu-id="71c15-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="71c15-133">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="71c15-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="71c15-134">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="71c15-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="71c15-135">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="71c15-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71c15-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71c15-136">Requirements</span></span>



| <span data-ttu-id="71c15-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c15-137">Requirement</span></span> | <span data-ttu-id="71c15-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c15-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c15-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c15-139">Minimum supported client</span></span><br/> | <span data-ttu-id="71c15-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c15-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="71c15-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c15-141">Minimum supported server</span></span><br/> | <span data-ttu-id="71c15-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c15-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="71c15-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="71c15-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="71c15-144"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71c15-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="71c15-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71c15-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="71c15-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71c15-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="71c15-147">DLL</span><span class="sxs-lookup"><span data-stu-id="71c15-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c15-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="71c15-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="71c15-149">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="71c15-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="71c15-150">**EnumPrintProcessorsW** (Unicode) et **EnumPrintProcessorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="71c15-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="71c15-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71c15-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c15-152">Impression</span><span class="sxs-lookup"><span data-stu-id="71c15-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="71c15-153">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="71c15-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="71c15-154">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="71c15-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="71c15-155">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="71c15-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="71c15-156">**\_Informations PRINTPROCESSOR \_ 1**</span><span class="sxs-lookup"><span data-stu-id="71c15-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

