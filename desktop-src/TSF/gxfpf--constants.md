---
title: Constantes GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes spécifient la position de caractère à retourner en fonction des coordonnées d’écran du point par rapport à un cadre englobant de caractère.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193499"
---
# <a name="gxfpf_-constants"></a>\_ \* CONSTANTEs GXFPF

Les \_ \* constantes GXFPF spécifient la position de caractère à retourner en fonction des coordonnées d’écran du point par rapport à un cadre englobant de caractère.



| Constante/valeur                                                                                                                                                                                                                                | Description                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ ARRONDI \_ le plus proche**</dt> <dt>(0x1)</dt> </dl> | Si les coordonnées d’écran du point sont contenues dans un cadre englobant de caractère, la position de caractère retournée est le bord englobant le plus proche des coordonnées d’écran du point.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ Le plus proche**</dt> <dt>(0X2)</dt> </dl>                    | Si les coordonnées d’écran du point ne sont pas contenues dans un cadre englobant de caractère, la position de caractère la plus proche est retournée.<br/>                                                      |



## <a name="remarks"></a>Notes

Les paramètres *dwFlags* des méthodes [ITextStoreACP :: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) et [ITfContextOwner :: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) utilisent ces constantes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITextStoreACP :: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





