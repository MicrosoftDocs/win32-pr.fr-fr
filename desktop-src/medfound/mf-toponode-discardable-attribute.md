---
description: Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Attribut MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531757"
---
# <a name="mf_toponode_discardable-attribute"></a>\_ \_ Attribut supprimable MF TOPONODE

Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds. En général, vous définissez cet attribut sur les nœuds tee pour indiquer que les sorties secondaires ne sont pas essentielles.

La valeur de l’attribut est un tableau d’index vers des flux de sortie sur le nœud.

Si cet attribut est défini, le pipeline peut supprimer des échantillons des flux de sortie spécifiés, si le flux est en retard.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

 

 




