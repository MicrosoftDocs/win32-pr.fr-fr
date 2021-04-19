---
description: La fonction AddPrintProvidor installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: AddPrintProvidor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518459"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="94a3f-103">AddPrintProvidor fonction)</span><span class="sxs-lookup"><span data-stu-id="94a3f-103">AddPrintProvidor function</span></span>

<span data-ttu-id="94a3f-104">La fonction **AddPrintProvidor** installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94a3f-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94a3f-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="94a3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94a3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a3f-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a3f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a3f-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le fournisseur doit être installé.</span><span class="sxs-lookup"><span data-stu-id="94a3f-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="94a3f-109">Pour les systèmes qui prennent uniquement en charge l’installation locale de fournisseurs, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="94a3f-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94a3f-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a3f-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a3f-111">Niveau de la structure vers laquelle *pProviderInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="94a3f-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="94a3f-112">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="94a3f-112">It can be one of the following.</span></span>



| <span data-ttu-id="94a3f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="94a3f-113">Value</span></span>                                                                                                | <span data-ttu-id="94a3f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="94a3f-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="94a3f-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="94a3f-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="94a3f-116">La fonction utilise une structure [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="94a3f-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="94a3f-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="94a3f-118">La fonction utilise une structure [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="94a3f-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94a3f-119">*pProviderInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94a3f-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a3f-120">Pointeur vers une structure de fournisseur d’impression, comme indiqué par *Level*.</span><span class="sxs-lookup"><span data-stu-id="94a3f-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a3f-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94a3f-121">Return value</span></span>

<span data-ttu-id="94a3f-122">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="94a3f-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="94a3f-123">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="94a3f-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a3f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="94a3f-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94a3f-125">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="94a3f-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="94a3f-126">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="94a3f-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="94a3f-127">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="94a3f-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="94a3f-128">Avant qu’une application appelle la fonction **AddPrintProvidor** , tous les fichiers requis par le fournisseur doivent être copiés dans le répertoire system32.</span><span class="sxs-lookup"><span data-stu-id="94a3f-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="94a3f-129">Un fournisseur ajouté par **AddPrintProvidor** peut être supprimé en appelant [**DeletePrintProvidor**](deleteprintprovidor.md).</span><span class="sxs-lookup"><span data-stu-id="94a3f-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a3f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94a3f-130">Requirements</span></span>



| <span data-ttu-id="94a3f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94a3f-131">Requirement</span></span> | <span data-ttu-id="94a3f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="94a3f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a3f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="94a3f-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94a3f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="94a3f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="94a3f-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94a3f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="94a3f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="94a3f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="94a3f-138"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94a3f-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="94a3f-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94a3f-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="94a3f-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94a3f-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="94a3f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="94a3f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a3f-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="94a3f-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="94a3f-143">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="94a3f-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="94a3f-144">**AddPrintProvidorW** (Unicode) et **AddPrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="94a3f-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="94a3f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94a3f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a3f-146">Impression</span><span class="sxs-lookup"><span data-stu-id="94a3f-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="94a3f-147">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="94a3f-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="94a3f-148">**DeletePrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="94a3f-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="94a3f-149">**\_Informations PROVIDOR \_ 1**</span><span class="sxs-lookup"><span data-stu-id="94a3f-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="94a3f-150">**\_Informations PROVIDOR \_ 2**</span><span class="sxs-lookup"><span data-stu-id="94a3f-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




