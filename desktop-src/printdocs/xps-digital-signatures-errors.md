---
description: Le tableau suivant répertorie toutes les valeurs HRESULT qui peuvent être retournées par les méthodes dans l’API de signature numérique XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Erreurs de l’API de signature numérique XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e40cea4b7d0e9997157c8b18c7f364ac7ac58b2b9edc6faec62cbe98685fcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711359"
---
# <a name="xps-digital-signature-api-errors"></a>Erreurs de l’API de signature numérique XPS

Le tableau suivant répertorie toutes les valeurs **HRESULT** qui peuvent être retournées par les méthodes dans l’API de signature numérique XPS. Notez que toutes les méthodes ne peuvent pas retourner toutes les valeurs de retour listées dans ce tableau.



| Code/valeur de retour                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>                                                                                                                                                                 | S_OK<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E 0x8052038b de \_ \_ \_ balise SIGNATUREBLOCK non valide**</dt> <dt></dt> </dl> | Une erreur s’est produite dans le balisage XML du bloc de signature lors de la lecture du balisage de signature.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ \_Éléments de \_ compatibilité \_ du balisage E**</dt> <dt>0x80520389</dt> </dl> | La valeur des [**\_ \_ indicateurs de signe XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) a spécifié qu’aucun élément de compatibilité du balisage n’était attendu ; Toutefois, des éléments de compatibilité du balisage ont été trouvés.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ objet \_ détaché**</dt> <dt>0x8052038a</dt> </dl>                                            | L’interface n’est pas associée au gestionnaire de signature.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ \_Package E \_ déjà \_ ouvert**</dt> <dt>0x80520387</dt> </dl>                      | Un package XPS a déjà été ouvert dans le gestionnaire de signature. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ \_Package E \_ non \_ ouvert**</dt> <dt>0x80520386</dt> </dl>                                  | Un package XPS n’a pas encore été ouvert dans le gestionnaire de signature. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Au moins deux signatures ont le même ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | L’ID de demande de signature n’est pas unique dans le bloc de signature.<br/>                                                                                                     |



 

## <a name="remarks"></a>Remarques

Certaines méthodes de l’API de signature numérique XPS effectuent des appels à l’API de création de [package](/previous-versions/windows/desktop/opc/packaging) . Pour plus d’informations sur les valeurs de retour de l’API de Packaging, consultez [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                            |
| En-tête<br/>                   | <dl> <dt>XpsDigitalSignature. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>XpsDigitalSignature. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestion des erreurs dans COM](../com/error-handling-in-com.md)
</dt> <dt>

[Erreurs d’empaquetage](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valeurs de retour de chiffrement](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

