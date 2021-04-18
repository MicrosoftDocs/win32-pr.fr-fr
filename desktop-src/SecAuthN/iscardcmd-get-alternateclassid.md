---
description: Récupère la valeur de l’ID de classe de substitution.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'ISCardCmd :: get_AlternateClassId, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542974"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="43232-103">ISCardCmd :: \_ AlternateClassId, méthode</span><span class="sxs-lookup"><span data-stu-id="43232-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="43232-104">\[La méthode **obtenir \_ AlternateClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="43232-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43232-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="43232-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43232-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="43232-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="43232-107">La méthode **obtenir \_ AlternateClassId** récupère la valeur de l’ID de classe de substitution.</span><span class="sxs-lookup"><span data-stu-id="43232-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="43232-108">Cette méthode échouera à moins que l’ID de remplacement ait été défini par un appel précédent à [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="43232-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43232-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43232-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="43232-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43232-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43232-111">*pbyClass* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="43232-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43232-112">Pointeur désignant l’octet qui contient la valeur d’ID de classe de remplacement au retour.</span><span class="sxs-lookup"><span data-stu-id="43232-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43232-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43232-113">Return value</span></span>

<span data-ttu-id="43232-114">La méthode retourne les valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="43232-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="43232-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43232-115">Return code</span></span>                                                                                    | <span data-ttu-id="43232-116">Description</span><span class="sxs-lookup"><span data-stu-id="43232-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43232-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43232-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="43232-118">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="43232-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="43232-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="43232-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="43232-120">Le paramètre *pbyClass* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="43232-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="43232-121"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="43232-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="43232-122">L’ID de classe de remplacement n’a pas été précédemment défini par un appel à [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="43232-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43232-123">Notes</span><span class="sxs-lookup"><span data-stu-id="43232-123">Remarks</span></span>

<span data-ttu-id="43232-124">Cette méthode s’applique aux communications utilisant le [*protocole T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="43232-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="43232-125">Pour plus d’informations, consultez [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="43232-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="43232-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="43232-126">Examples</span></span>

<span data-ttu-id="43232-127">L’exemple suivant montre comment récupérer l’ID de classe de substitution.</span><span class="sxs-lookup"><span data-stu-id="43232-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="43232-128">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="43232-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="43232-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43232-129">Requirements</span></span>



| <span data-ttu-id="43232-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43232-130">Requirement</span></span> | <span data-ttu-id="43232-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="43232-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43232-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43232-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43232-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43232-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="43232-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43232-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43232-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43232-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43232-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="43232-136">End of client support</span></span><br/>    | <span data-ttu-id="43232-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="43232-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="43232-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="43232-138">End of server support</span></span><br/>    | <span data-ttu-id="43232-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43232-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="43232-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="43232-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="43232-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="43232-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="43232-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="43232-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="43232-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43232-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43232-144">DLL</span><span class="sxs-lookup"><span data-stu-id="43232-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43232-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43232-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="43232-146">IID</span><span class="sxs-lookup"><span data-stu-id="43232-146">IID</span></span><br/>                      | <span data-ttu-id="43232-147">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="43232-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="43232-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43232-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43232-149">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="43232-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="43232-150">**put \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="43232-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
