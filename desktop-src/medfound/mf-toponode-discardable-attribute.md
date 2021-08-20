---
description: Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Attribut MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658ee92433b4f0f24d01d7d0b3c0396e4ba1d46b4d2841b0619c8c9a5b15c46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875173"
---
# <a name="mf_toponode_discardable-attribute"></a>\_ \_ Attribut supprimable MF TOPONODE

Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique à tous les types de nœuds. En général, vous définissez cet attribut sur les nœuds tee pour indiquer que les sorties secondaires ne sont pas essentielles.

La valeur de l’attribut est un tableau d’index vers des flux de sortie sur le nœud.

Si cet attribut est défini, le pipeline peut supprimer des échantillons des flux de sortie spécifiés, si le flux est en retard.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




