---
title: Constantes WINBIO_EVENT ( \_ types WINBIO. h)
description: Spécifiez les types de notifications d’événements du fournisseur de services à surveiller.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508373"
---
# <a name="winbio_event-constants"></a>\_Constantes d’événement WINBIO

Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) pour spécifier les types de notifications d’événements du fournisseur de services à surveiller.



| Constante                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**\_événement WINBIO \_ FP \_ récupéré**</dt> </dl>                             | Le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus. Le Windows Biometric Framework appelle la fonction de rappel pour indiquer qu’un glissement Finger s’est produit, mais n’essaie pas d’identifier l’empreinte digitale.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**identification de l' \_ événement WINBIO \_ FP \_ inréclamée \_**</dt> </dl> | Le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus. Le Windows Biometric Framework tente d’identifier l’empreinte digitale et transmet le résultat de ce processus à votre fonction de rappel.<br/>                        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





