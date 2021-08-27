---
description: définit le pic &\# 0034 ; compartiment à fuite&\# 0034 ; paramètres (consultez la section notes) pour l’encodage d’un fichier multimédia Windows. Ces paramètres sont utilisés pour le taux binaire de pointe. Définissez cet attribut à l’aide de l’interface IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Attribut MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060839"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>\_ \_ Attribut LEAKYBUCKET2 ASFSTREAMCONFIG MF

définit le pic des paramètres du compartiment perdu (consultez la section notes) pour l’encodage d’un fichier multimédia Windows. Ces paramètres sont utilisés pour le taux binaire de pointe. Définissez cet attribut à l’aide de l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un tableau de trois **DWORD**, dans l’ordre suivant :

-   Vitesse de transmission, en bits par seconde.
-   Fenêtre de mémoire tampon, en millisecondes.
-   Saturation de la mémoire tampon initiale, en octets.

pour plus d’informations sur le concept de compartiment avec fuites, consultez la rubrique [modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md) perdu dans la documentation du kit de développement logiciel (SDK) de Format de média Windows.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




