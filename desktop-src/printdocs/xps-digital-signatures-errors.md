---
description: Le tableau suivant répertorie toutes les valeurs HRESULT qui peuvent être retournées par les méthodes dans l’API de signature numérique XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Erreurs de l’API de signature numérique XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320261"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="e2b5f-103">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="e2b5f-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="e2b5f-104">Le tableau suivant répertorie toutes les valeurs **HRESULT** qui peuvent être retournées par les méthodes dans l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="e2b5f-105">Notez que toutes les méthodes ne peuvent pas retourner toutes les valeurs de retour listées dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="e2b5f-106">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e2b5f-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="e2b5f-107">Description</span><span class="sxs-lookup"><span data-stu-id="e2b5f-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="e2b5f-108"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="e2b5f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2b5f-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="e2b5f-110"><dt>**XPS \_ E 0x8052038b de \_ \_ \_ balise SIGNATUREBLOCK non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="e2b5f-111">Une erreur s’est produite dans le balisage XML du bloc de signature lors de la lecture du balisage de signature.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="e2b5f-112"><dt>**XPS \_ \_Éléments de \_ compatibilité \_ du balisage E**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="e2b5f-113">La valeur des [**\_ \_ indicateurs de signe XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) a spécifié qu’aucun élément de compatibilité du balisage n’était attendu ; Toutefois, des éléments de compatibilité du balisage ont été trouvés.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="e2b5f-114"><dt>**XPS \_ E \_ objet \_ détaché**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="e2b5f-115">L’interface n’est pas associée au gestionnaire de signature.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="e2b5f-116"><dt>**XPS \_ \_Package E \_ déjà \_ ouvert**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="e2b5f-117">Un package XPS a déjà été ouvert dans le gestionnaire de signature.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="e2b5f-118"><dt>**XPS \_ \_Package E \_ non \_ ouvert**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="e2b5f-119">Un package XPS n’a pas encore été ouvert dans le gestionnaire de signature.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="e2b5f-120"><dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="e2b5f-121">Au moins deux signatures ont le même ID.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="e2b5f-122"><dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="e2b5f-123">L’ID de demande de signature n’est pas unique dans le bloc de signature.</span><span class="sxs-lookup"><span data-stu-id="e2b5f-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="e2b5f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e2b5f-124">Remarks</span></span>

<span data-ttu-id="e2b5f-125">Certaines méthodes de l’API de signature numérique XPS effectuent des appels à l’API de création de [package](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="e2b5f-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="e2b5f-126">Pour plus d’informations sur les valeurs de retour de l’API de Packaging, consultez [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="e2b5f-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b5f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2b5f-127">Requirements</span></span>



| <span data-ttu-id="e2b5f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2b5f-128">Requirement</span></span> | <span data-ttu-id="e2b5f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2b5f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b5f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2b5f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b5f-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2b5f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="e2b5f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2b5f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b5f-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2b5f-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e2b5f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2b5f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b5f-135"><dt>XpsDigitalSignature. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2b5f-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="e2b5f-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2b5f-137"><dt>XpsDigitalSignature. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2b5f-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b5f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2b5f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b5f-139">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="e2b5f-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="e2b5f-140">Erreurs d’empaquetage</span><span class="sxs-lookup"><span data-stu-id="e2b5f-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="e2b5f-141">Valeurs de retour de chiffrement</span><span class="sxs-lookup"><span data-stu-id="e2b5f-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

