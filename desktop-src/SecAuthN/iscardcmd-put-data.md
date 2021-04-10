---
description: Définit le champ de données dans l’unité de données du protocole d’application (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: ISCardCmd ::p ut_Data, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114143"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="fbf65-103">ISCardCmd ::p \_ méthode de données ut</span><span class="sxs-lookup"><span data-stu-id="fbf65-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="fbf65-104">\[La méthode **put \_ Data** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="fbf65-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbf65-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fbf65-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbf65-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fbf65-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fbf65-107">La méthode **put \_ Data** définit le champ de données dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="fbf65-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf65-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf65-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="fbf65-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf65-110">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbf65-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf65-111">Pointeur vers l’objet de mémoire tampon d’octets (**IStream**) à copier dans le champ de données APDU.</span><span class="sxs-lookup"><span data-stu-id="fbf65-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf65-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf65-112">Return value</span></span>

<span data-ttu-id="fbf65-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="fbf65-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fbf65-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fbf65-114">Return code</span></span>                                                                                   | <span data-ttu-id="fbf65-115">Description</span><span class="sxs-lookup"><span data-stu-id="fbf65-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="fbf65-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fbf65-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fbf65-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="fbf65-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fbf65-119">Le paramètre *pData* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fbf65-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fbf65-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fbf65-121">Un pointeur incorrect a été passé dans *pData*.</span><span class="sxs-lookup"><span data-stu-id="fbf65-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="fbf65-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fbf65-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="fbf65-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="fbf65-124">Notes</span><span class="sxs-lookup"><span data-stu-id="fbf65-124">Remarks</span></span>

<span data-ttu-id="fbf65-125">Lorsque vous définissez une nouvelle partie des données du message, la longueur du champ de données est calculée et stockée dans le paramètre P3 du APDU.</span><span class="sxs-lookup"><span data-stu-id="fbf65-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="fbf65-126">Pour récupérer la longueur du champ de données, appelez [**obtenir \_ P3**](iscardcmd-get-p3.md).</span><span class="sxs-lookup"><span data-stu-id="fbf65-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="fbf65-127">Pour récupérer le champ de données de l’APDU, appelez [**obtenir des \_ données**](iscardcmd-get-data.md).</span><span class="sxs-lookup"><span data-stu-id="fbf65-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fbf65-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="fbf65-128">Examples</span></span>

<span data-ttu-id="fbf65-129">L’exemple suivant montre comment définir le champ de données dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="fbf65-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="fbf65-130">L’exemple suppose que pIByteData est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) , et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf65-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fbf65-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf65-131">Requirements</span></span>



| <span data-ttu-id="fbf65-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf65-132">Requirement</span></span> | <span data-ttu-id="fbf65-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf65-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf65-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf65-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf65-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf65-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fbf65-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf65-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf65-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf65-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbf65-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fbf65-138">End of client support</span></span><br/>    | <span data-ttu-id="fbf65-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbf65-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fbf65-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fbf65-140">End of server support</span></span><br/>    | <span data-ttu-id="fbf65-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbf65-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fbf65-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf65-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf65-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbf65-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fbf65-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbf65-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fbf65-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf65-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf65-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf65-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbf65-148">IID</span><span class="sxs-lookup"><span data-stu-id="fbf65-148">IID</span></span><br/>                      | <span data-ttu-id="fbf65-149">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fbf65-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fbf65-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf65-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf65-151">**récupérer des \_ données**</span><span class="sxs-lookup"><span data-stu-id="fbf65-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="fbf65-152">**Accédez à \_ P3**</span><span class="sxs-lookup"><span data-stu-id="fbf65-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="fbf65-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="fbf65-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
