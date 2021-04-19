---
description: Spécifie un nouvel identificateur de classe de remplacement dans l’unité de données du protocole d’application (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: ISCardCmd ::p ut_AlternateClassId, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514025"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="fffea-103">ISCardCmd ::p ut \_ AlternateClassId, méthode</span><span class="sxs-lookup"><span data-stu-id="fffea-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="fffea-104">\[La méthode **put \_ AlternateClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="fffea-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fffea-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fffea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fffea-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fffea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fffea-107">La méthode **put \_ AlternateClassId** spécifie un nouvel identificateur de classe de remplacement dans le protocole APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="fffea-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="fffea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fffea-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="fffea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fffea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fffea-110">*byClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fffea-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fffea-111">Autre identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="fffea-111">Alternate class identifier.</span></span> <span data-ttu-id="fffea-112">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="fffea-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffea-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fffea-113">Return value</span></span>

<span data-ttu-id="fffea-114">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="fffea-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fffea-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fffea-115">Return code</span></span>                                                                                  | <span data-ttu-id="fffea-116">Description</span><span class="sxs-lookup"><span data-stu-id="fffea-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fffea-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fffea-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fffea-118">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fffea-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="fffea-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fffea-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fffea-120">Le paramètre *byClass* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fffea-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fffea-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fffea-121">Remarks</span></span>

<span data-ttu-id="fffea-122">Avec les communications utilisant le [*protocole T = 0*](../secgloss/t-gly.md), les commandes de carte supplémentaires peuvent être générées automatiquement par le APDU et envoyées à l’unité de données de protocole de transmission (TPDU).</span><span class="sxs-lookup"><span data-stu-id="fffea-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="fffea-123">Les commandes supplémentaires utilisent généralement le même ID de classe que la commande d’origine. la spécification d’un nouvel ID de classe au moyen de cette méthode permet aux commandes générées automatiquement d’utiliser le nouvel ID de classe.</span><span class="sxs-lookup"><span data-stu-id="fffea-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="fffea-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="fffea-124">Examples</span></span>

<span data-ttu-id="fffea-125">L’exemple suivant montre comment définir un nouvel identificateur de classe de remplacement dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="fffea-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="fffea-126">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="fffea-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fffea-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fffea-127">Requirements</span></span>



| <span data-ttu-id="fffea-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fffea-128">Requirement</span></span> | <span data-ttu-id="fffea-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fffea-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fffea-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fffea-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fffea-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fffea-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fffea-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fffea-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fffea-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fffea-134">End of client support</span></span><br/>    | <span data-ttu-id="fffea-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fffea-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fffea-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fffea-136">End of server support</span></span><br/>    | <span data-ttu-id="fffea-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fffea-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fffea-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="fffea-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffea-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="fffea-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fffea-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fffea-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fffea-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fffea-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fffea-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fffea-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffea-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffea-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fffea-144">IID</span><span class="sxs-lookup"><span data-stu-id="fffea-144">IID</span></span><br/>                      | <span data-ttu-id="fffea-145">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fffea-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fffea-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fffea-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffea-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="fffea-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="fffea-148">**Obtient \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="fffea-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
