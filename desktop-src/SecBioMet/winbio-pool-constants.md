---
title: Constantes WINBIO_POOL ( \_ types WINBIO. h)
description: Spécifiez le type de pool d’unités biométriques à utiliser dans la session.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509406"
---
# <a name="winbio_pool-constants"></a>\_Constantes de pool WINBIO

Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier le type de pool d’unités biométriques à utiliser dans la session.



| Constante                                                                                                                                                                                  | Description                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ inconnu**</dt> </dl>          | Le type de pool est inconnu.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_système de pool WINBIO \_**</dt> </dl>             | Spécifie une collection partagée d’unités biométriques gérées par le fournisseur de services.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**\_pool WINBIO \_ privé**</dt> </dl>          | Spécifie une collection d’unités biométriques gérées par l’appelant.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**\_pool WINBIO \_ non assigné**</dt> </dl> | Réservé.<br/>                                                                         |



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

 

 





