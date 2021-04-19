---
title: Méthode GetObjectDataOnClearChannel
description: La méthode GetObjectDataOnClearChannel transfère à Windows Media Gestionnaire de périphériques un bloc de données d’objet sur un canal clair.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Méthode GetObjectDataOnClearChannel Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535227"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="3922e-104">Méthode GetObjectDataOnClearChannel</span><span class="sxs-lookup"><span data-stu-id="3922e-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="3922e-105">La méthode **GetObjectDataOnClearChannel** transfère à Windows Media gestionnaire de périphériques un bloc de données d’objet sur un canal clair.</span><span class="sxs-lookup"><span data-stu-id="3922e-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="3922e-106">Cette méthode est identique à [**ISCPSecureExchange :: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , sauf que les données retournées par cette méthode ne sont pas chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3922e-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="3922e-107">Par conséquent, cette méthode est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="3922e-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="3922e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3922e-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="3922e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3922e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3922e-110">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="3922e-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3922e-111">Pointeur vers l’objet appareil.</span><span class="sxs-lookup"><span data-stu-id="3922e-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="3922e-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="3922e-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="3922e-113">Pointeur vers une mémoire tampon destinée à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="3922e-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="3922e-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="3922e-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3922e-115">Pointeur vers une **valeur DWORD** contenant la taille de transfert.</span><span class="sxs-lookup"><span data-stu-id="3922e-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3922e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3922e-116">Return value</span></span>

<span data-ttu-id="3922e-117">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3922e-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3922e-118">Si la méthode échoue, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3922e-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="3922e-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3922e-119">Return code</span></span>                                                                                                | <span data-ttu-id="3922e-120">Description</span><span class="sxs-lookup"><span data-stu-id="3922e-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3922e-121"><dt>**échec de la vérification de WMDM \_ E \_ Mac \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="3922e-122">Le code d’authentification du message n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3922e-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3922e-123"><dt>**WMDM \_ E \_ nojustes**</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="3922e-124">L’appelant ne dispose pas des droits nécessaires pour effectuer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="3922e-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="3922e-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="3922e-126">Échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3922e-126">The method failed.</span></span> <span data-ttu-id="3922e-127">Arrêtez l’interaction avec le fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="3922e-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="3922e-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="3922e-129">Un paramètre est un pointeur **null** ou non valide.</span><span class="sxs-lookup"><span data-stu-id="3922e-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3922e-130"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="3922e-131">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="3922e-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3922e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="3922e-132">Remarks</span></span>

<span data-ttu-id="3922e-133">Pour transférer des données, Windows Media Gestionnaire de périphériques appelle la méthode [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) pour obtenir les données du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3922e-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="3922e-134">**GetObjectDataOnClearChannel** est ensuite appelé pour transférer des blocs de données d’objet du fournisseur de contenu vers Windows Media gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="3922e-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="3922e-135">Si l' \_ opération S OK est retournée avec *pdwSize* défini à zéro, Windows Media gestionnaire de périphériques demandera aucune autre donnée.</span><span class="sxs-lookup"><span data-stu-id="3922e-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="3922e-136">Cette méthode est identique à [**ISCPSecureExchange :: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , sauf que les données retournées par cette méthode ne sont pas chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3922e-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="3922e-137">Par conséquent, cette méthode est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="3922e-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="3922e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3922e-138">Requirements</span></span>



| <span data-ttu-id="3922e-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3922e-139">Requirement</span></span> | <span data-ttu-id="3922e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3922e-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3922e-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="3922e-141">Header</span></span><br/>  | <dl> <span data-ttu-id="3922e-142"><dt>WMSCP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="3922e-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3922e-143">Library</span></span><br/> | <dl> <span data-ttu-id="3922e-144"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3922e-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3922e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3922e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3922e-146">**ISCPSecureExchange :: ObjectData**</span><span class="sxs-lookup"><span data-stu-id="3922e-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="3922e-147">**Interface ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="3922e-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





