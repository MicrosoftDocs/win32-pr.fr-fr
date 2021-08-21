---
description: Obtient les statistiques du récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Attribut MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a80bf0682cf6e46845a968122bf512a6e9cff15df8fb8e0312e1c63c8dab0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973618"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>Attribut des statistiques de \_ MP2DLNA MF \_

Obtient les statistiques du récepteur multimédia DLNA (Digital vivant Network Alliance).

## <a name="data-type"></a>Type de données

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stocké en tant qu' **octet \[ \]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

## <a name="remarks"></a>Remarques

Pendant la diffusion en continu, le récepteur multimédia DLNA met à jour cet attribut avec des statistiques sur l’encodage et le multiplexage des flux MPEG-2. L’application peut interroger cet attribut à tout moment pour obtenir les valeurs les plus récentes.

La définition de cet attribut sur le récepteur multimédia DLNA n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




