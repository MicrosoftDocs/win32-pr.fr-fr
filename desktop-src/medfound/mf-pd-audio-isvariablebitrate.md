---
description: Spécifie si les flux audio d’une présentation ont une vitesse de transmission variable.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: Attribut MF_PD_AUDIO_ISVARIABLEBITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5c8c15c12bcd867342fb11f5e753c196f9954aea0393b2a461e1804f411339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664189"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>\_Attribut ISVARIABLEBITRATE de l’audio MF PD \_ \_

Spécifie si les flux audio d’une présentation ont une vitesse de transmission variable.

## <a name="data-type"></a>Type de données

**uint32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S'applique à

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut facultatif pour les descripteurs de présentation. Si l’attribut a la **valeur true** (différente de zéro), la présentation contient au moins un flux audio VBR (variable-bit-rate). Si l’attribut a la **valeur false**, tous les flux audio ont une vitesse de transmission constante.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




