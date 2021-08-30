---
description: Cette section fournit les spécifications de référence pour les constantes de manipulation directe.
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: Constantes de manipulation directe
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c99a9423eb84d2889307c4433ea5e6b8d941435710894116da3201b71b71ee8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094679"
---
# <a name="direct-manipulation-constants"></a>Constantes de manipulation directe

Cette section fournit les spécifications de référence pour les constantes de [manipulation directe](direct-manipulation-portal.md) .

| Constante/valeur                                                                                                                                                                                                                                                                         | Description                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <dt>**DIRECTMANIPULATION \_ KEYBOARDFOCUS**</dt> <dt>0xfffffffe</dt> </dl> | Spécifie un ID de pointeur Psuedo pour émuler un contact tactile via une entrée au clavier.<br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <dt>**DIRECTMANIPULATION \_ MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt> </dl>          | Spécifie un ID de pointeur Psuedo pour émuler un contact tactile via l’entrée de la souris.<br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <dt>**DIRECTMANIPULATION \_ \_Zoom minimal**</dt> <dt>0,1</dt> </dl>          | Spécifie la limite de zoom minimale autorisée de 10%.<br/>                               |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                              |
| MIDL<br/>                      | <dl> <dt>DirectManipulation. idl</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Référence de manipulation directe](direct-manipulation-reference.md)
