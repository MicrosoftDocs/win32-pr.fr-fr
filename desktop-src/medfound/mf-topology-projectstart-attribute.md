---
description: Spécifie l’heure d’arrêt d’une topologie, par rapport au début de la première topologie dans la séquence.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Attribut MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863581"
---
# <a name="mf_topology_projectstart-attribute"></a>\_Attribut PROJECTSTART de la topologie MF \_

Spécifie l’heure d’arrêt d’une topologie, par rapport au début de la première topologie dans la séquence.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Notes

La valeur est donnée en unités de nanosecondes de 100.

Si la session multimédia a été créée avec l’attribut d' [**\_ \_ \_ heure globale de session MF**](mf-session-global-time-attribute.md) de la **valeur true**, toutes les topologies doivent contenir l’attribut **\_ \_ PROJECTSTART de topologie MF** . Dans le cas contraire, les topologies ne doivent pas contenir l’attribut **\_ \_ PROJECTSTART** de topologie MF. Pour plus d’informations, consultez [durée de présentation des séquences](sequence-presentation-times.md).

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Durée des présentations de séquence](sequence-presentation-times.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_PROJECTSTOP de topologie \_ MF**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




