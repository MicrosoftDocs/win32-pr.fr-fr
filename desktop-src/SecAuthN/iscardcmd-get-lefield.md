---
description: Retourne le champ le de l’unité de données de protocole d’application (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'ISCardCmd :: get_LeField, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760113"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="21128-103">ISCardCmd :: \_ LeField, méthode</span><span class="sxs-lookup"><span data-stu-id="21128-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="21128-104">\[La méthode **obtenir \_ LeField** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="21128-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21128-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="21128-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="21128-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="21128-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="21128-107">La méthode d' **extraction \_ LeField** retourne le champ le de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="21128-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="21128-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21128-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="21128-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21128-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21128-110">*plSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21128-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21128-111">Pointeur vers la valeur du champ le au retour.</span><span class="sxs-lookup"><span data-stu-id="21128-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21128-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21128-112">Return value</span></span>

<span data-ttu-id="21128-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="21128-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="21128-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="21128-114">Return code</span></span>                                                                                  | <span data-ttu-id="21128-115">Description</span><span class="sxs-lookup"><span data-stu-id="21128-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="21128-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21128-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="21128-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="21128-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="21128-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="21128-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="21128-119">Le paramètre *plSize* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="21128-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="21128-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="21128-120">Examples</span></span>

<span data-ttu-id="21128-121">L’exemple suivant montre comment récupérer la valeur du champ le à partir de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="21128-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="21128-122">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="21128-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="21128-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21128-123">Requirements</span></span>



| <span data-ttu-id="21128-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21128-124">Requirement</span></span> | <span data-ttu-id="21128-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="21128-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21128-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21128-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21128-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21128-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="21128-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21128-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21128-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21128-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21128-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="21128-130">End of client support</span></span><br/>    | <span data-ttu-id="21128-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21128-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="21128-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="21128-132">End of server support</span></span><br/>    | <span data-ttu-id="21128-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21128-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="21128-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="21128-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="21128-135"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="21128-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="21128-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="21128-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="21128-137"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21128-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21128-138">DLL</span><span class="sxs-lookup"><span data-stu-id="21128-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21128-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21128-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21128-140">IID</span><span class="sxs-lookup"><span data-stu-id="21128-140">IID</span></span><br/>                      | <span data-ttu-id="21128-141">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="21128-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="21128-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21128-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21128-143">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="21128-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
