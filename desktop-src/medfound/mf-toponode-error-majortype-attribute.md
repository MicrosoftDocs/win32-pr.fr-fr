---
description: Contient le type de média principal pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Attribut MF_TOPONODE_ERROR_MAJORTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544240"
---
# <a name="mf_toponode_error_majortype-attribute"></a>\_Attribut MAJORTYPE de l’erreur TOPONODE MF \_ \_

Contient le type de média principal pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds.

Le chargeur de topologie peut définir l’attribut. Les applications lisent généralement cet attribut, mais ne la définissent pas.

Pour obtenir la liste des valeurs possibles, consultez [types de média majeurs](media-type-guids.md).

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

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




