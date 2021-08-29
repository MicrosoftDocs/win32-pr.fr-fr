---
description: Spécifie le type de charge utile d’un flux d’encodage audio avancé (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Attribut MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c4c7852e5719f2293e21f7f37c761c39a14dca132113c6b9224038c640e3d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940679"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>\_Attribut de \_ \_ type de charge utile MT MT AAC \_

Spécifie le type de charge utile d’un flux d’encodage audio avancé (AAC).

## <a name="data-type"></a>Type de données

**UINT32**

Les valeurs suivantes sont possibles.



| Valeur                                                                        | Signification                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Le flux contient uniquement des éléments de bloc de données brutes \_ \_ .<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Flux de transport des données audio (ADTS). Le flux contient une \_ séquence ADTS, telle que définie par MPEG-2.<br/>                       |
| <dl> <dt>2</dt> </dl> | Format d’échange de données audio (ADIF). Le flux contient une \_ séquence ADIF, telle que définie par MPEG-2.<br/>                     |
| <dl> <dt>3</dt> </dl> | Le flux contient un flux de transport audio MPEG-4 avec une couche de synchronisation (garantie) et une couche multiplex (LATM).<br/> |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S'applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarques

Le \_ type de charge utile de l’option MF MT \_ AAC \_ \_ est facultatif. Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments de bloc de données brutes \_ \_ .

S’applique uniquement à **MFAudioFormat \_ AAC**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




