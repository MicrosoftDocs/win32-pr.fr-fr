---
title: Constantes diverses de service de texte TSF (Ctffunc. h)
description: Les valeurs suivantes sont utilisées avec les services de texte.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd4d9cdd73cd42512fe667b84867328c65f13fafa7281341eca7ba6379eef7d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476769"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>Constantes diverses de service de texte TSF

Les valeurs suivantes sont utilisées avec les services de texte.



| Constante/valeur                                                                                                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**Tf \_ MENUREADY**</dt> <dt>0x00000001</dt> </dl>                                                | Pas utilisé pour l'instant.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**Tf \_ \_État PROPUI \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | La propriété peut être sérialisée. Si cette valeur n’est pas présente, la propriété ne peut pas être sérialisée. Cette valeur est utilisée avec [ITfFnPropertyUIStatus :: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) et [ITfFnPropertyUIStatus :: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITfFnPropertyUIStatus :: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus :: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





