---
description: Spécifie l’entrée actuelle dans la zone de description de l’exemple pour un type de média MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Attribut MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236183"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>\_Attribut d' \_ entrée d’exemple de \_ \_ \_ ligne de code MPEG4 MF

Spécifie l’entrée actuelle dans la zone de description de l’exemple pour un type de média MPEG-4.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Notes

Dans un fichier MP4 ou 3GP, la zone Description de l’exemple décrit l’encodage utilisé pour un flux dans le fichier. La zone Description de l’exemple peut contenir plusieurs entrées. Cet attribut spécifie l’entrée à utiliser. La valeur est un index de base zéro dans la liste.

Actuellement, la seule valeur prise en charge est 0. L’attribut a été défini pour une future extensibilité.

La source du fichier MPEG-4 définit toujours la valeur sur 0. Les récepteurs de fichiers MP4 et 3GP ignorent la valeur de cet attribut si elle est présente.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[\_Exemple de \_ Description du MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




