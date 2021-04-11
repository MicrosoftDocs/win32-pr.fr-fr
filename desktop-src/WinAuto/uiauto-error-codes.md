---
title: Codes d’erreur (UIAutomationCoreApi. h)
description: Cette rubrique décrit les codes d’erreur exposés par Microsoft UI Automation.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032284"
---
# <a name="error-codes-uiautomationcoreapih"></a>Codes d’erreur (UIAutomationCoreApi. h)

Cette rubrique décrit les codes d’erreur exposés par Microsoft UI Automation. La liste est triée par ordre alphabétique par nom.



| Constante/valeur                                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ \_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | Indique qu’une méthode a été appelée sur un élément virtualisé, ou sur un élément qui n’existe plus, généralement parce qu’elle a été détruite. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ \_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | Indique qu’une méthode qui requiert un élément activé, tel que [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) ou [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), a été appelée sur un élément qui a été désactivé. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | Indique que la méthode a tenté une opération qui n’était pas valide.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ \_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt> </dl>                   | Indique que la méthode [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) a été appelée sur un élément qui n’a pas de point cliquable.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ \_NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | Indique que le fournisseur ne prend pas en charge explicitement la propriété ou le modèle de contrôle spécifié. UI Automation renverra ce code d’erreur à l’appelant sans tenter de fournir une valeur par défaut ou de revenir à un autre fournisseur.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ \_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | Indique qu’un problème s’est produit lors du chargement d’un assembly qui contient un fournisseur côté client (proxy).<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ \_Délai d’expiration E**</dt> <dt>0x80131505</dt> </dl>                                                      | Indique que le temps alloué à un processus ou une opération a expiré.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                             |
| En-tête<br/>                   | <dl> <dt>UIAutomationCoreApi. h</dt> </dl> |



 

 





