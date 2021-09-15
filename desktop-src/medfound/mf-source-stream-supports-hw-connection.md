---
description: Indique si une source de média prend en charge le workflow de données matérielles.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Attribut MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523624"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>Le \_ flux source MF \_ \_ prend en charge l' \_ attribut de \_ connexion HW

Indique si une source de média prend en charge le workflow de données matérielles.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Cet attribut est utilisé quand une source de média transmet un périphérique matériel et est en mesure de transférer des données en aval sur un bus matériel, sans envoyer de données jusqu’au processeur. Par exemple, une webcam peut fournir une vidéo encodée H. 264 directement à un décodeur matériel intégré.

Dans ce scénario, la source et le décodeur sont toujours représentés dans le Microsoft Media Foundation par un objet de [source multimédia](media-sources.md) et une table de [Media Foundation de transformation](media-foundation-transforms.md) (MFT). Toutefois, il n’y a pas de flux de données entre ces deux objets au niveau de la couche de pipeline, uniquement au niveau de la couche matérielle, comme indiqué dans le diagramme suivant.

![diagramme qui montre une source de proxy matériel.](images/proxy-mft3.png)

La connexion entre la source du média et la table MFT est négociée comme suit.

1.  Le pipeline interroge la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) . (Cette interface est facultative pour la prise en charge des sources multimédias.)
2.  Le pipeline appelle [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Les requêtes de pipeline pour \_ le \_ flux source MF \_ prennent en charge l' \_ attribut de connexion HW \_ . Si l’attribut est présent et qu’il est égal à **true**, la source du média prend en charge les connexions matérielles.
4.  Le pipeline vérifie si la MFT est également un proxy matériel, en vérifiant l’attribut d' [ \_ \_ \_ \_ attribut d’URL matériel de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur la table MFT. Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).
5.  Le pipeline définit l’attribut d' [ \_ \_ \_ attribut de flux connecté MFT](mft-connected-stream-attribute.md) sur la table MFT. La valeur de cet attribut est le pointeur [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtenu à partir de la source du média à l’étape 2.
6.  Le pipeline affecte la **valeur true** à la [table MFT \_ connectée à l’attribut de \_ \_ \_ flux matériel](mft-connected-to-hw-stream.md) à la fois à la source du média et à la table MFT.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> </dl>

 

 




