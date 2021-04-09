---
description: Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud topologie.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Attribut MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114027"
---
# <a name="mf_toponode_errorcode-attribute"></a>\_Attribut ERRORCODE d’TOPONODE MF \_

Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud topologie.

## <a name="data-type"></a>Type de données

**UINT32**

Ttreat en tant que valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds.

La valeur de cet attribut est une valeur **HRESULT** .

La session multimédia ou le chargeur topologique peut définir l’attribut. Les applications lisent généralement cet attribut, mais ne la définissent pas.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




