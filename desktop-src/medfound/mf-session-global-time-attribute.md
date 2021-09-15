---
description: Spécifie si les topologies ont une heure de début et de fin globale.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Attribut MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523633"
---
# <a name="mf_session_global_time-attribute"></a>\_Attribut de \_ durée globale de session MF \_

Spécifie si les topologies ont une heure de début et de fin globale.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Vous pouvez définir cet attribut lorsque vous créez le média sesison à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si cet attribut est présent et différent de zéro, toutes les topologies transmises à la session de média doivent avoir les attributs de topologie [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) et de [**\_ topologie MF \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . Ces attributs spécifient les heures de début et de fin de la topologie par rapport à l’ensemble de la présentation.

Si cet attribut est absent ou **false**, les topologies ne doivent pas avoir l’attribut de topologie [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) ou MF de topologie [**MF \_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .

Utilisez cet attribut pour créer des séquences de modification. Pour plus d’informations, consultez [durée de présentation des séquences](sequence-presentation-times.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de session multimédia](media-session-attributes.md)
</dt> <dt>

[Durée des présentations de séquence](sequence-presentation-times.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**\_PROJECTSTART de topologie \_ MF**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**\_PROJECTSTOP de topologie \_ MF**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




