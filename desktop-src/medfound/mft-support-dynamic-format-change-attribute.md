---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge les modifications de format dynamiques.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Attribut MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012609"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>\_Attribut de \_ \_ modification du format dynamique \_ de la MFT

Spécifie si une Media Foundation transformation (MFT) prend en charge les modifications de format dynamiques.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut peut avoir les valeurs suivantes.



| Valeur     | Description                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Le client peut modifier le format d’entrée pendant la diffusion en continu.               |
| **FALSE** | La table MFT doit être vidée pour que le client puisse modifier le format d’entrée. |



 

Pour obtenir cet attribut, appelez d’abord [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global pour la table MFT. Appelez ensuite [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour récupérer la valeur de l’attribut.

Si [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) échoue ou si l’attribut n’est pas présent, la valeur par défaut est **false**.

Un [MFTS asynchrone](asynchronous-mfts.md) doit retourner la valeur **true**.

Pour plus d’informations, consultez [gestion des modifications de flux](handling-stream-changes.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




