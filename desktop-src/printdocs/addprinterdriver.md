---
description: La fonction AddPrinterDriver installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: AddPrinterDriver, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757858"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="fe8e2-103">AddPrinterDriver fonction)</span><span class="sxs-lookup"><span data-stu-id="fe8e2-103">AddPrinterDriver function</span></span>

<span data-ttu-id="fe8e2-104">La fonction **AddPrinterDriver** installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="fe8e2-105">Pour une plus grande flexibilité lors de l’installation ou de la mise à niveau des pilotes d’imprimante, utilisez la fonction [**AddPrinterDriverEx**](addprinterdriverex.md) car elle permet une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers plus récents uniquement et la copie de tous les fichiers (quels que soient les horodatages de fichier).</span><span class="sxs-lookup"><span data-stu-id="fe8e2-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="fe8e2-106">L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="fe8e2-107">Utilisez [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe8e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe8e2-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fe8e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe8e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8e2-110">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe8e2-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8e2-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote doit être installé.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="fe8e2-112">Si *pname* a la **valeur null**, le pilote est installé localement.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="fe8e2-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe8e2-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8e2-114">Version de la structure vers laquelle *pDriverInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="fe8e2-115">Cette valeur peut être 2, 3, 4, 6 ou 8.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="fe8e2-116">*pDriverInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe8e2-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8e2-117">Pointeur vers une structure contenant des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="fe8e2-118">Cela dépend de la valeur de *Level*.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="fe8e2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe8e2-119">Value</span></span> | <span data-ttu-id="fe8e2-120">Structure du lecteur d’imprimante</span><span class="sxs-lookup"><span data-stu-id="fe8e2-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="fe8e2-121">2</span><span class="sxs-lookup"><span data-stu-id="fe8e2-121">2</span></span>     | [<span data-ttu-id="fe8e2-122">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="fe8e2-123">3</span><span class="sxs-lookup"><span data-stu-id="fe8e2-123">3</span></span>     | [<span data-ttu-id="fe8e2-124">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="fe8e2-125">4</span><span class="sxs-lookup"><span data-stu-id="fe8e2-125">4</span></span>     | [<span data-ttu-id="fe8e2-126">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="fe8e2-127">6</span><span class="sxs-lookup"><span data-stu-id="fe8e2-127">6</span></span>     | [<span data-ttu-id="fe8e2-128">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="fe8e2-129">8</span><span class="sxs-lookup"><span data-stu-id="fe8e2-129">8</span></span>     | [<span data-ttu-id="fe8e2-130">**\_Informations sur le pilote \_ 8**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="fe8e2-131">Si le membre **pEnvironment** de la structure vers laquelle pointe *PDriverInfo* a la **valeur null**, l’environnement actuel de l’appelant/client (et non du serveur/de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8e2-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe8e2-132">Return value</span></span>

<span data-ttu-id="fe8e2-133">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fe8e2-134">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8e2-135">Notes</span><span class="sxs-lookup"><span data-stu-id="fe8e2-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe8e2-136">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fe8e2-137">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fe8e2-138">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fe8e2-139">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="fe8e2-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="fe8e2-140">Avant qu’une application appelle la fonction **AddPrinterDriver** , tous les fichiers requis par le pilote doivent être copiés dans le répertoire du pilote d’imprimante du système.</span><span class="sxs-lookup"><span data-stu-id="fe8e2-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="fe8e2-141">Une application peut récupérer le nom de ce répertoire en appelant la fonction [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8e2-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="fe8e2-142">Une application peut déterminer les pilotes d’imprimante actuellement installés en appelant la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8e2-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8e2-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe8e2-143">Requirements</span></span>



| <span data-ttu-id="fe8e2-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe8e2-144">Requirement</span></span> | <span data-ttu-id="fe8e2-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe8e2-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8e2-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe8e2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8e2-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe8e2-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe8e2-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe8e2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8e2-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe8e2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe8e2-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe8e2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8e2-151"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe8e2-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fe8e2-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe8e2-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe8e2-153"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe8e2-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fe8e2-154">DLL</span><span class="sxs-lookup"><span data-stu-id="fe8e2-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe8e2-155"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fe8e2-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fe8e2-156">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fe8e2-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe8e2-157">**AddPrinterDriverW** (Unicode) et **AddPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe8e2-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="fe8e2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe8e2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8e2-159">Impression</span><span class="sxs-lookup"><span data-stu-id="fe8e2-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-160">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="fe8e2-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-161">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-162">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-163">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-164">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-165">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-166">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="fe8e2-167">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="fe8e2-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

