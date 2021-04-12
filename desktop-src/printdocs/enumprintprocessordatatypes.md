---
description: La fonction EnumPrintProcessorDatatypes énumère les types de données pris en charge par un processeur d’impression spécifié.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: EnumPrintProcessorDatatypes, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529001"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="1520e-103">EnumPrintProcessorDatatypes fonction)</span><span class="sxs-lookup"><span data-stu-id="1520e-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="1520e-104">La fonction **EnumPrintProcessorDatatypes** énumère les types de données pris en charge par un processeur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="1520e-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="1520e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1520e-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="1520e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1520e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1520e-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1520e-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le processeur d’impression réside.</span><span class="sxs-lookup"><span data-stu-id="1520e-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="1520e-109">Si ce paramètre a la **valeur null**, les types de données du processeur d’impression local sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="1520e-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-110">*pPrintProcessorName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1520e-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression dont les types de données sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="1520e-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-112">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1520e-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-113">Type d’informations retournées dans la mémoire tampon *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="1520e-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="1520e-114">Ce paramètre doit être 1.</span><span class="sxs-lookup"><span data-stu-id="1520e-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-115">*pDatatypes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1520e-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-116">Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations de types de données \_ \_ 1**](datatypes-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="1520e-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="1520e-117">Chaque structure décrit un type de données disponible.</span><span class="sxs-lookup"><span data-stu-id="1520e-117">Each structure describes an available data type.</span></span> <span data-ttu-id="1520e-118">La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="1520e-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="1520e-119">Pour déterminer la taille de mémoire tampon requise, appelez **EnumPrintProcessorDatatypes** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="1520e-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="1520e-120">**EnumPrintProcessorDatatypes** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="1520e-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-121">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1520e-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-122">Taille, en octets, de la mémoire tampon vers laquelle pointe *pDatatypes*.</span><span class="sxs-lookup"><span data-stu-id="1520e-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-123">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1520e-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-124">Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pDatatypes* si la fonction est réussie.</span><span class="sxs-lookup"><span data-stu-id="1520e-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="1520e-125">Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="1520e-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="1520e-126">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1520e-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1520e-127">Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="1520e-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="1520e-128">Il s’agit du nombre de types de données pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1520e-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1520e-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1520e-129">Return value</span></span>

<span data-ttu-id="1520e-130">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1520e-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1520e-131">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1520e-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1520e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="1520e-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1520e-133">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="1520e-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1520e-134">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="1520e-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1520e-135">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="1520e-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1520e-136">v</span><span class="sxs-lookup"><span data-stu-id="1520e-136">v</span></span>

<span data-ttu-id="1520e-137">À compter de Windows Vista, les informations sur le type de données des serveurs d’impression distants sont récupérées à partir d’un cache local.</span><span class="sxs-lookup"><span data-stu-id="1520e-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="1520e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1520e-138">Requirements</span></span>



| <span data-ttu-id="1520e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1520e-139">Requirement</span></span> | <span data-ttu-id="1520e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1520e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1520e-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1520e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1520e-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1520e-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1520e-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1520e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1520e-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1520e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1520e-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="1520e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1520e-146"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1520e-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1520e-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1520e-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="1520e-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1520e-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1520e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1520e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1520e-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1520e-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1520e-151">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1520e-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1520e-152">**EnumPrintProcessorDatatypesW** (Unicode) et **EnumPrintProcessorDatatypesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1520e-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1520e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1520e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1520e-154">Impression</span><span class="sxs-lookup"><span data-stu-id="1520e-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1520e-155">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="1520e-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1520e-156">**Informations de type de données \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1520e-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="1520e-157">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="1520e-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

