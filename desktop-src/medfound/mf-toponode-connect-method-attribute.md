---
description: Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Attribut MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313886"
---
# <a name="mf_toponode_connect_method-attribute"></a>\_Attribut de \_ méthode de connexion MF TOPONODE \_

Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds.

La valeur d’attribut est une **opération or au niveau du bit** des indicateurs de l’énumération de [**\_ \_ méthode MF Connect**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) . Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ Connect \_ autoriser le \_ décodeur**.

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

 

 




