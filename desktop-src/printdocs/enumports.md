---
description: La fonction EnumPorts énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: EnumPorts, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529191"
---
# <a name="enumports-function"></a><span data-ttu-id="35aff-103">EnumPorts fonction)</span><span class="sxs-lookup"><span data-stu-id="35aff-103">EnumPorts function</span></span>

<span data-ttu-id="35aff-104">La fonction **EnumPorts** énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="35aff-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="35aff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35aff-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="35aff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35aff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35aff-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35aff-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur dont vous souhaitez énumérer les ports d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="35aff-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="35aff-109">Si *pname* a la **valeur null**, la fonction énumère les ports d’imprimante de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="35aff-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="35aff-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35aff-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-111">Type d’informations retournées dans la mémoire tampon *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="35aff-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="35aff-112">Si le *niveau* est 1, *pPorts* reçoit un tableau de structures d' [**informations de port \_ \_ 1**](port-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="35aff-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="35aff-113">Si le *niveau* est 2, *pPorts* reçoit un tableau de structures d' [**informations de port \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="35aff-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="35aff-114">*pPorts* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35aff-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-115">Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations de port \_ \_ 1**](port-info-1.md) ou d' [**informations de port \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="35aff-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="35aff-116">Chaque structure contient des données qui décrivent un port d’imprimante disponible.</span><span class="sxs-lookup"><span data-stu-id="35aff-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="35aff-117">La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="35aff-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="35aff-118">Pour déterminer la taille de mémoire tampon requise, appelez **EnumPorts** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="35aff-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="35aff-119">**EnumPorts** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="35aff-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="35aff-120">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35aff-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-121">Taille, en octets, de la mémoire tampon vers laquelle pointe *pPorts*.</span><span class="sxs-lookup"><span data-stu-id="35aff-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="35aff-122">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35aff-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-123">Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="35aff-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="35aff-124">Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="35aff-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="35aff-125">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35aff-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35aff-126">Pointeur vers une variable qui reçoit le nombre de structures [**d' \_ informations \_ de port 1**](port-info-1.md) ou d' [**informations de port \_ \_ 2**](port-info-2.md) retournées dans la mémoire tampon *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="35aff-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="35aff-127">Il s’agit du nombre de ports d’imprimante disponibles sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="35aff-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35aff-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35aff-128">Return value</span></span>

<span data-ttu-id="35aff-129">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="35aff-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="35aff-130">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="35aff-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35aff-131">Notes</span><span class="sxs-lookup"><span data-stu-id="35aff-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35aff-132">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="35aff-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="35aff-133">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="35aff-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="35aff-134">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="35aff-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="35aff-135">La fonction **EnumPorts** peut être exécutée même si le serveur spécifié par *pname* n’a pas d’imprimante définie.</span><span class="sxs-lookup"><span data-stu-id="35aff-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="35aff-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35aff-136">Requirements</span></span>



| <span data-ttu-id="35aff-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35aff-137">Requirement</span></span> | <span data-ttu-id="35aff-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="35aff-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35aff-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35aff-139">Minimum supported client</span></span><br/> | <span data-ttu-id="35aff-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35aff-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="35aff-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35aff-141">Minimum supported server</span></span><br/> | <span data-ttu-id="35aff-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35aff-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="35aff-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="35aff-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="35aff-144"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35aff-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="35aff-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35aff-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="35aff-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35aff-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="35aff-147">DLL</span><span class="sxs-lookup"><span data-stu-id="35aff-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35aff-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="35aff-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="35aff-149">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="35aff-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35aff-150">**EnumPortsW** (Unicode) et **EnumPortsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35aff-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="35aff-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35aff-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35aff-152">Impression</span><span class="sxs-lookup"><span data-stu-id="35aff-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="35aff-153">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="35aff-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="35aff-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="35aff-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="35aff-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="35aff-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="35aff-156">**\_Informations sur le port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="35aff-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="35aff-157">**\_Informations sur le port \_ 2**</span><span class="sxs-lookup"><span data-stu-id="35aff-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

