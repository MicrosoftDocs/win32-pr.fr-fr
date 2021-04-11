---
description: Ouvre une instance d’un fournisseur de tickets d’impression.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202702"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="797ce-103">BindPTProviderThunk fonction)</span><span class="sxs-lookup"><span data-stu-id="797ce-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="797ce-104">\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="797ce-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="797ce-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]</span><span class="sxs-lookup"><span data-stu-id="797ce-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="797ce-106">Ouvre une instance d’un fournisseur de tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="797ce-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="797ce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="797ce-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="797ce-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="797ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="797ce-109">*pszPrinterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="797ce-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="797ce-110">Nom complet d’une file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="797ce-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="797ce-111">*MaxVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="797ce-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="797ce-112">La dernière version du [schéma d’impression](./printschema.md) que l’appelant prend en charge.</span><span class="sxs-lookup"><span data-stu-id="797ce-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="797ce-113">*prefVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="797ce-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="797ce-114">Version du schéma d' [impression](./printschema.md) demandé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="797ce-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="797ce-115">*phProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="797ce-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="797ce-116">Pointeur vers un handle du fournisseur de tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="797ce-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="797ce-117">*usedVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="797ce-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="797ce-118">Version du schéma d' [impression](./printschema.md) que le fournisseur de tickets d’impression utilisera.</span><span class="sxs-lookup"><span data-stu-id="797ce-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="797ce-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="797ce-119">Return value</span></span>

<span data-ttu-id="797ce-120">Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="797ce-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="797ce-121">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="797ce-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="797ce-122">Notes</span><span class="sxs-lookup"><span data-stu-id="797ce-122">Remarks</span></span>

<span data-ttu-id="797ce-123">Avant d’appeler cette fonction, le thread appelant doit initialiser COM en appelant [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="797ce-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="797ce-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="797ce-124">Requirements</span></span>



| <span data-ttu-id="797ce-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="797ce-125">Requirement</span></span> | <span data-ttu-id="797ce-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="797ce-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="797ce-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="797ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="797ce-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="797ce-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="797ce-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="797ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="797ce-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="797ce-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="797ce-131">DLL</span><span class="sxs-lookup"><span data-stu-id="797ce-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="797ce-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="797ce-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="797ce-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="797ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797ce-134">Schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="797ce-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="797ce-135">**PTOpenProviderEx**</span><span class="sxs-lookup"><span data-stu-id="797ce-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="797ce-136">Impression</span><span class="sxs-lookup"><span data-stu-id="797ce-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="797ce-137">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="797ce-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

