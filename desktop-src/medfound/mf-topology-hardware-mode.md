---
description: Spécifie s’il faut charger des transformations de Microsoft Media Foundation matérielles (MFTs) dans la topologie.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Attribut MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875666"
---
# <a name="mf_topology_hardware_mode-attribute"></a>\_ \_ Attribut de mode matériel \_ de la topologie MF

Spécifie s’il faut charger des transformations de Microsoft Media Foundation matérielles (MFTs) dans la topologie.

## <a name="data-type"></a>Type de données

**[**MFTOPOLOGY \_ \_Mode matériel**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. Définissez l’attribut avant de résoudre la topologie.



| Valeur                                  | Description                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ use \_ Hardware**  | Le chargeur de topologie chargera les MFTs matériels, tels que les décodeurs matériels, lorsqu’ils sont disponibles.<br/> Le chargeur de topologie revient automatiquement au décodage logiciel si aucun décodeur matériel n’est trouvé, ou si un décodeur matériel ne parvient pas à se connecter pour une raison quelconque.<br/> |
| **MFTOPOLOGY \_ HWMODE \_ Software \_ uniquement** | Le chargeur de topologie chargera uniquement les MFTss logicielles, y compris les décodeurs logiciels.                                                                                                                                                                                                    |



 

La valeur par défaut est **MFTOPOLOGY \_ HWMODE \_ Software \_ uniquement**, pour la compatibilité avec les applications existantes. La valeur recommandée est **MFTOPOLOGY \_ HWMODE \_ use \_ Hardware**.

Si le chargeur de topologie insère une table MFT matérielle dans la topologie, il définit l’attribut d' [ \_ attribut d' \_ \_ URL matériel \_ de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur le nœud de topologie. Pour vérifier si une table MFT matérielle est présente, énumérez les nœuds dans la topologie résolue et vérifiez si cet attribut est présent.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




