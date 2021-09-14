---
title: Constantes TF_SS_ (msctf. h)
description: Les \_ \_ constantes TF SS \, définies avant l’exécution dans la \_ structure d’État TF, décrivent les États des documents statiques.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416333"
---
# <a name="tf_ss_-constants"></a>\_ \_ \* Constantes TF SS

Les \_ \_ \* constantes TF SS, définies avant l’exécution dans la structure d' [**\_ État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , décrivent les États des documents statiques.



| Constante/valeur                                                                                                                                                                                                                                                                              | Description                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**Tf \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt> </dl>                                     | Le document prend en charge les sélections multiples.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**Tf \_ \_zones SS**</dt> <dt>(zones de sécurité Terminal Server \_ \_ )</dt> </dl>                                                     | Le document peut contenir plusieurs régions.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**Tf \_ SS \_ transitoire**</dt> <dt>(TS \_ SS \_ transitif)</dt> </dl>                                         | Le document est supposé avoir un cycle d’utilisation courts.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**Tf \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt> </dl> | **À partir de Windows 8 :** Le document prend en charge la correction automatique fournie par le clavier tactile.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**Tf \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt> </dl>     | **À partir de Windows 8 :** Le document prend en charge les suggestions de texte fournies par le clavier tactile.<br/> |



## <a name="remarks"></a>Notes

Le membre **dwStaticFlags** de la \_ structure d’État TF utilise ces constantes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_État TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

