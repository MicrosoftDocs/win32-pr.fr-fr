---
description: La fonction EnumMonitors récupère des informations sur les moniteurs de port installés sur le serveur spécifié.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: EnumMonitors, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756400"
---
# <a name="enummonitors-function"></a><span data-ttu-id="fb133-103">EnumMonitors fonction)</span><span class="sxs-lookup"><span data-stu-id="fb133-103">EnumMonitors function</span></span>

<span data-ttu-id="fb133-104">La fonction **EnumMonitors** récupère des informations sur les moniteurs de port installés sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="fb133-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb133-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb133-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="fb133-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb133-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb133-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel les analyses résident.</span><span class="sxs-lookup"><span data-stu-id="fb133-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="fb133-109">Si ce paramètre a la **valeur null**, les analyses locales sont énumérées.</span><span class="sxs-lookup"><span data-stu-id="fb133-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="fb133-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb133-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-111">Version de la structure vers laquelle pointe *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="fb133-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="fb133-112">Cette valeur peut être 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="fb133-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fb133-113">*pMonitors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb133-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-114">Pointeur vers une mémoire tampon qui reçoit un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="fb133-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="fb133-115">La mémoire tampon doit être suffisamment grande pour stocker les chaînes référencées par les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="fb133-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="fb133-116">Pour déterminer la taille de mémoire tampon requise, appelez **EnumMonitors** avec *cbBuf* défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="fb133-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="fb133-117">**EnumMonitors** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.</span><span class="sxs-lookup"><span data-stu-id="fb133-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="fb133-118">La mémoire tampon reçoit un tableau de structures [**information d’analyse \_ \_ 1**](monitor-info-1.md) si le *niveau* est 1, ou [**Surveillez les structures \_ info \_ 2**](monitor-info-2.md) si le *niveau* est 2.</span><span class="sxs-lookup"><span data-stu-id="fb133-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="fb133-119">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb133-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-120">Taille, en octets, de la mémoire tampon vers laquelle pointe *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="fb133-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="fb133-121">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb133-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-122">Pointeur vers une variable qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="fb133-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="fb133-123">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb133-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb133-124">Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon vers laquelle pointe *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="fb133-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb133-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb133-125">Return value</span></span>

<span data-ttu-id="fb133-126">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="fb133-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fb133-127">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="fb133-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb133-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fb133-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb133-129">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fb133-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fb133-130">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="fb133-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fb133-131">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="fb133-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb133-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb133-132">Requirements</span></span>



| <span data-ttu-id="fb133-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb133-133">Requirement</span></span> | <span data-ttu-id="fb133-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb133-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb133-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb133-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fb133-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb133-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fb133-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb133-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fb133-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb133-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fb133-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb133-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb133-140"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb133-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fb133-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb133-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb133-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb133-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fb133-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fb133-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb133-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fb133-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fb133-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fb133-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fb133-146">**EnumMonitorsW** (Unicode) et **EnumMonitorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fb133-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="fb133-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb133-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb133-148">Impression</span><span class="sxs-lookup"><span data-stu-id="fb133-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fb133-149">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="fb133-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fb133-150">**\_Informations sur le moniteur \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fb133-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="fb133-151">**\_Informations sur le moniteur \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fb133-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

