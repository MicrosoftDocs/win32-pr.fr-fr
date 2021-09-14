---
description: Permet au convertisseur vidéo amélioré (EVR) d’améliorer les performances en ignorant le deuxième champ de chaque trame entrelacée.
ms.assetid: de7efc6a-19ae-4f3a-8675-38fda3c979e2
title: Attribut EVRConfig_AllowDropToHalfInterlace (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9989fe833ea763166ba870c331add5c18bcb45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122161"
---
# <a name="evrconfig_allowdroptohalfinterlace-attribute"></a>\_Attribut EVRConfig AllowDropToHalfInterlace

Permet au convertisseur vidéo amélioré (EVR) d’améliorer les performances en ignorant le deuxième champ de chaque trame entrelacée.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut peut être défini sur le récepteur multimédia EVR. Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoMixPrefs \_ ALLOWDROPTOHALFINTERLACE** sur EVR. Pour obtenir une description de cet indicateur, consultez [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .

La constante GUID de cet attribut est exportée à partir de strmiids. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestion de la qualité vidéo](video-quality-management.md)
</dt> </dl>

 

 




