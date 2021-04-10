---
title: Constantes de magasin de texte diverses (Textstor. h)
description: Les constantes du magasin de texte divers définissent certaines propriétés pour les magasins de texte.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105400"
---
# <a name="miscellaneous-text-store-constants"></a>Constantes de magasin de texte diverses

Les constantes du magasin de texte divers définissent certaines propriétés pour les magasins de texte.



| Constante/valeur                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ \_Sélection par défaut**</dt> <dt>((ULONG)-1)</dt> </dl> | Si le paramètre *ulIndex* de [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) est défini sur cette valeur, la sélection par défaut est obtenue.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ GEA \_ masqué**</dt> <dt>(0x1)</dt> </dl>                              | Si le paramètre *dwFlags* de [ITextStoreAnchor :: GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) est défini sur cette valeur, un objet incorporé peut être localisé dans le texte masqué.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ masqué**</dt> <dt>(0x1)</dt> </dl>                              | Non utilisé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ \_Correction St**</dt> <dt>(0x1)</dt> </dl>                     | Si le paramètre *dwFlags* de [ITextStoreACP :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)ou [ITextStoreACPSink :: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) est défini sur cette valeur, le texte est une transformation (correction) du contenu existant et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ \_Correction TC**</dt> <dt>(0x1)</dt> </dl>                     | Si le paramètre *dwFlags* de [ITextStoreAnchorSink :: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) est défini sur cette valeur, le texte est une transformation (correction) du contenu existant, et toutes les informations de balisage de texte spéciales (métadonnées) sont conservées, telles que les données de fichier. wav ou un identificateur de langue.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ nul**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                    | Utilisé en interne par TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink :: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Constantes d’infrastructure diverses](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





