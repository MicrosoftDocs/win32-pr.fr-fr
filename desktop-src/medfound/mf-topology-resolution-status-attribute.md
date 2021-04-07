---
description: Spécifie l’état d’une tentative de résolution d’une topologie.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Attribut MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863578"
---
# <a name="mf_topology_resolution_status-attribute"></a>\_Attribut état de la résolution de la topologie MF \_ \_

Spécifie l’état d’une tentative de résolution d’une topologie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Le chargeur de topologie ou la session de média peut définir cet attribut sur une topologie. La valeur de cet attribut est **une opération or au niveau du bit** de l’énumération d' [**indicateurs d’état de \_ résolution de topologie \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




