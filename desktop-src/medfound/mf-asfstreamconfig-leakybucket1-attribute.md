---
description: Définit la moyenne &\# 0034 ; compartiment à fuite&\# 0034 ; paramètres (consultez la section Notes) pour l’encodage d’un fichier Windows Media. Définissez cet attribut à l’aide de l’interface IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Attribut MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529744"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>\_ \_ Attribut LEAKYBUCKET1 ASFSTREAMCONFIG MF

Définit les paramètres de la « plage perdue » moyenne (consultez la section Notes) pour l’encodage d’un fichier Windows Media. Définissez cet attribut à l’aide de l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

La valeur de cet attribut est un tableau de trois **DWORD**, dans l’ordre suivant :

-   Vitesse de transmission, en bits par seconde.
-   Fenêtre de mémoire tampon, en millisecondes.
-   Saturation de la mémoire tampon initiale, en octets.

Pour plus d’informations sur le concept de compartiment avec fuites, consultez la rubrique [modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md) perdu dans la documentation du kit de développement logiciel (SDK) Windows Media format.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
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

 

 




