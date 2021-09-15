---
description: Indique quelle sortie est la sortie principale sur un nœud tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Attribut MF_TOPONODE_PRIMARYOUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530697"
---
# <a name="mf_toponode_primaryoutput-attribute"></a>\_ \_ Attribut PRIMARYOUTPUT, car TOPONODE MF

Indique quelle sortie est la sortie principale sur un nœud tee.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds tee (**\_ \_ \_ nœud tee de topologie MF**).

La valeur de cet attribut est l’index de base zéro d’une connexion de sortie sur ce nœud tee. Cette valeur indique la sortie qui est le flux de sortie principal. Le pipeline attend une demande de la sortie principale avant de traiter les demandes des autres sorties.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




