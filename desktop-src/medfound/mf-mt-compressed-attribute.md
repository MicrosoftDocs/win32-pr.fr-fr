---
description: Spécifie pour un type de support si les données multimédia sont compressées.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Attribut MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127314029"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Attribut compressé MF MT

Spécifie pour un type de support si les données multimédia sont compressées.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le type de média est un format compressé. Dans le cas contraire, le type de média est décompressé ou le type de compression n’est pas connu.

Il n’est pas garanti que cet attribut soit défini sur **true** pour tous les formats compressés, donc les applications ne doivent généralement pas utiliser cet attribut. La méthode la plus fiable pour déterminer si un format est compressé consiste à conserver une liste de formats connus. Si une application ne reconnaît pas un format, comme spécifié dans l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) , elle ne doit pas prendre en part la compression du format.

Pour déterminer si un format utilise la compression temporelle (ce qui signifie que certains échantillons sont calculés comme des deltas à partir d’exemples précédents), vérifiez l’attribut de l’attribut [**MF \_ MT \_ All \_ Samples \_ Independent**](mf-mt-all-samples-independent-attribute.md) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




