---
description: Spécifie l’adresse de nœud (NAD) à utiliser avec l’interface ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: ISCardCmd ::p ut_Nad, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863265"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="5daa0-103">ISCardCmd : méthode :p ut \_ nad</span><span class="sxs-lookup"><span data-stu-id="5daa0-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="5daa0-104">\[La méthode **put \_ nad** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5daa0-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5daa0-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5daa0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5daa0-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5daa0-107">La méthode **put \_ nad** spécifie l’adresse de nœud (NAD) à utiliser avec l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="5daa0-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="5daa0-108">Cela s’applique aux communications utilisant uniquement les communications de [*protocole T = 1*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5daa0-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="5daa0-109">Par défaut, l’objet [**ISCardCmd**](iscardcmd.md) utilise un nad de zéro.</span><span class="sxs-lookup"><span data-stu-id="5daa0-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="5daa0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5daa0-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="5daa0-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5daa0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5daa0-112">*bNad* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5daa0-113">Octet représentant le NAD à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5daa0-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5daa0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5daa0-114">Return value</span></span>

<span data-ttu-id="5daa0-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="5daa0-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5daa0-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5daa0-116">Return code</span></span>                                                                                  | <span data-ttu-id="5daa0-117">Description</span><span class="sxs-lookup"><span data-stu-id="5daa0-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5daa0-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5daa0-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5daa0-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5daa0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5daa0-121">Le paramètre *bNad* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5daa0-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="5daa0-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5daa0-122">Remarks</span></span>

<span data-ttu-id="5daa0-123">Cette méthode doit être appelée uniquement lorsqu’il est nécessaire d’utiliser une valeur autre que zéro pour le NAD.</span><span class="sxs-lookup"><span data-stu-id="5daa0-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="5daa0-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="5daa0-124">Examples</span></span>

<span data-ttu-id="5daa0-125">L’exemple suivant montre comment spécifier une adresse de nœud à utiliser avec l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="5daa0-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="5daa0-126">L’exemple suppose que byNadValue est une variable de type **Byte** à laquelle une valeur a été précédemment affectée, et que pISCardCmd est un pointeur valide vers une instance de l’interface **ISCardCmd** .</span><span class="sxs-lookup"><span data-stu-id="5daa0-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5daa0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5daa0-127">Requirements</span></span>



| <span data-ttu-id="5daa0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5daa0-128">Requirement</span></span> | <span data-ttu-id="5daa0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5daa0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5daa0-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5daa0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5daa0-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5daa0-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5daa0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5daa0-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5daa0-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5daa0-134">End of client support</span></span><br/>    | <span data-ttu-id="5daa0-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5daa0-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5daa0-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5daa0-136">End of server support</span></span><br/>    | <span data-ttu-id="5daa0-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5daa0-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5daa0-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="5daa0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5daa0-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5daa0-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5daa0-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="5daa0-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5daa0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5daa0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5daa0-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5daa0-144">IID</span><span class="sxs-lookup"><span data-stu-id="5daa0-144">IID</span></span><br/>                      | <span data-ttu-id="5daa0-145">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5daa0-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5daa0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5daa0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5daa0-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="5daa0-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
