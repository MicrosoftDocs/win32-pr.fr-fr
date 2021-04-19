---
description: La fonction DeletePrinterDriver supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: DeletePrinterDriver, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517821"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="20c81-103">DeletePrinterDriver fonction)</span><span class="sxs-lookup"><span data-stu-id="20c81-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="20c81-104">La fonction **DeletePrinterDriver** supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="20c81-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="20c81-105">Pour supprimer les fichiers associés au pilote en plus de supprimer le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge pour un serveur, utilisez la fonction [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="20c81-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="20c81-106">**DeletePrinterDriver** supprime un pilote uniquement si aucune version du pilote n’est utilisée pour l’environnement spécifié.</span><span class="sxs-lookup"><span data-stu-id="20c81-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="20c81-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) peut supprimer des versions spécifiques du pilote.</span><span class="sxs-lookup"><span data-stu-id="20c81-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c81-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20c81-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="20c81-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20c81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c81-110">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c81-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le pilote doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="20c81-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="20c81-112">Si ce paramètre a la **valeur null**, le nom du pilote d’imprimante est supprimé localement.</span><span class="sxs-lookup"><span data-stu-id="20c81-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-113">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c81-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le pilote doit être supprimé (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="20c81-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="20c81-115">Si ce paramètre a la **valeur null**, le nom du pilote est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).</span><span class="sxs-lookup"><span data-stu-id="20c81-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="20c81-116">*pDriverName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c81-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote qui doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="20c81-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c81-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20c81-118">Return value</span></span>

<span data-ttu-id="20c81-119">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="20c81-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="20c81-120">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="20c81-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c81-121">Notes</span><span class="sxs-lookup"><span data-stu-id="20c81-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20c81-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="20c81-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="20c81-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="20c81-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="20c81-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="20c81-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="20c81-125">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="20c81-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="20c81-126">La fonction **DeletePrinterDriver** ne supprime pas les fichiers associés, elle supprime simplement le nom du pilote de la liste retournée par la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="20c81-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="20c81-127">Avant d’appeler **DeletePrinterDriver**, vous devez supprimer tous les objets d’imprimante qui utilisent le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="20c81-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="20c81-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20c81-128">Requirements</span></span>



| <span data-ttu-id="20c81-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20c81-129">Requirement</span></span> | <span data-ttu-id="20c81-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="20c81-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c81-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="20c81-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20c81-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="20c81-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="20c81-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20c81-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20c81-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="20c81-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="20c81-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="20c81-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20c81-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="20c81-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="20c81-139">DLL</span><span class="sxs-lookup"><span data-stu-id="20c81-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20c81-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="20c81-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="20c81-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20c81-142">**DeletePrinterDriverW** (Unicode) et **DeletePrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20c81-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="20c81-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c81-144">Impression</span><span class="sxs-lookup"><span data-stu-id="20c81-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="20c81-145">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="20c81-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="20c81-146">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="20c81-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="20c81-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="20c81-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

