---
description: Contient le sous-type de média pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Attribut MF_TOPONODE_ERROR_SUBTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524078"
---
# <a name="mf_toponode_error_subtype-attribute"></a>\_Attribut de \_ sous-type d’erreur MF TOPONODE \_

Contient le sous-type de média pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds.

Le chargeur de topologie peut définir l’attribut. Les applications lisent généralement cet attribut, mais ne la définissent pas.

Pour obtenir la liste des valeurs possibles, consultez [GUID type Media](media-type-guids.md).

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

 

 




