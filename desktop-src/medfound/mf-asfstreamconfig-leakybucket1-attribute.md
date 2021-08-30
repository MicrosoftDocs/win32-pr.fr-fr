---
description: définit la moyenne &\# 0034 ; compartiment à fuite&\# 0034 ; paramètres (consultez la section notes) pour l’encodage d’un fichier multimédia Windows. Définissez cet attribut à l’aide de l’interface IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Attribut MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5343d7721d6fad4be4d8623ffdd8f1b3e63fccbe8d90cd4616e0115c35fc2100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826819"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>\_ \_ Attribut LEAKYBUCKET1 ASFSTREAMCONFIG MF

définit les paramètres de la « plage perdue » moyenne (consultez la section notes) pour l’encodage d’un fichier multimédia Windows. Définissez cet attribut à l’aide de l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

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



| Condition requise | Value |
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

[**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




