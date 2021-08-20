---
description: Spécifie si un objet sous-jacent de nœuds topologie est un Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Attribut MF_TOPONODE_DECRYPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e3bb58dd176e02f80d3e18e64c08c1e880e40c19179582e50cfac8927399da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875163"
---
# <a name="mf_toponode_decryptor-attribute"></a>\_Attribut de \_ déchiffreur MF TOPONODE

Spécifie si l’objet sous-jacent d’un nœud topologie est un Decrypter.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut s’applique à tous les types de nœuds.

Si la valeur de cet attribut est différente de zéro, l’objet sous-jacent du nœud est un Decrypter.

En général, les applications n’utilisent pas cet attribut directement. La session multimédia définit cet attribut lors de la création d’un nœud pour un Decrypter, obtenu à partir de la méthode [**IMFInputTrustAuthority :: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




