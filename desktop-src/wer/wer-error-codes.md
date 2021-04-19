---
title: Codes d’erreur WER (Werapi. h)
description: Le tableau suivant fournit une liste de codes d’erreur personnalisés utilisés par Rapport d’erreurs Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538608"
---
# <a name="wer-error-codes"></a>Codes d’erreur WER

Le tableau suivant fournit une liste de codes d’erreur personnalisés utilisés par Rapport d’erreurs Windows.



| Constante                                                                                                                                                                                            | Description                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <dt>**WER \_ E \_ tampon insuffisant \_**</dt> </dl> | Une mémoire tampon est trop petite pour contenir les données.<br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <dt>**WER \_ E \_ État non valide \_**</dt> </dl>                   | Une fonction a été appelée de manière non prise en charge.<br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <dt>**dépassement de la longueur du WER \_ E \_ \_**</dt> </dl>             | L’une des limites de longueur a été dépassée.<br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <dt>**WER \_ # \_ \_ param manquant**</dt> </dl>                   | Un ou plusieurs paramètres sont manquants.<br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <dt>**WER \_ E \_ non \_ trouvé**</dt> </dl>                               | Element not found.<br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <dt>**stock E/d WER \_ \_ \_ désactivé**</dt> </dl>                | Le magasin a été désactivé.<br/>                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Werapi. h</dt> </dl> |



 

 





