---
title: Styles de contrôle SysLink (CommCtrl. h)
description: Les constantes de style suivantes sont utilisées lors de la création de contrôles SysLink.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3707a4e7b59811a99cb23ca4ebdbfc8bc2d285c2e8780502241beebb2f7485d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670546"
---
# <a name="syslink-control-styles"></a>Styles de contrôle SysLink

Les constantes de style suivantes sont utilisées lors de la création de contrôles SysLink.



| Constante                                                                                                                                                                        | Description                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**LWS \_ transparent**</dt> </dl>             | Le mode de combinaison d’arrière-plan est transparent. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_ IGNORERETURN**</dt> </dl>       | Lorsque le lien a le focus clavier et que l’utilisateur appuie sur entrée, la touche est ignorée par le contrôle et transmise à la boîte de dialogue hôte.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**le \_ préfixe LWS**</dt> </dl>                      | **Windows Vista**. Si le texte contient une esperluette, il est traité comme un caractère littéral plutôt que le préfixe d’une touche de raccourci.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_ USEVISUALSTYLE**</dt> </dl> | **Windows Vista**. Le lien est affiché dans le style visuel actuel.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**\_USECUSTOMTEXT LWS**</dt> </dl>       | **Windows Vista**. Une [notification \_ CUSTOMTEXT nm](nm-customtext.md) est envoyée lorsque le contrôle est dessiné, afin que l’application puisse fournir du texte de manière dynamique.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ droit**</dt> </dl>                               | **Windows Vista**. Le texte est justifié à droite.<br/>                                                                                                                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





