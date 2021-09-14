---
description: Spécifie si le pipeline tronque les exemples.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Attribut MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296310"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>L' \_ attribut MARKOUT de la topologie MF \_ n’a pas de \_ marque \_

Spécifie si le pipeline tronque les exemples.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Par défaut, le pipeline tronque les échantillons pour qu’ils correspondent aux durées de présentation appropriées. La suppression est effectuée sur les nœuds de topologie qui ont les attributs [**\_ TOPONODE \_ \_**](mf-toponode-markin-here-attribute.md) et [**MF \_ TOPONODE \_ MARKOUT \_ ici**](mf-toponode-markout-here-attribute.md) . Si l' **attribut \_ \_ \_ \_ MARKOUT de la topologie MF** n’a pas la valeur **true** sur la topologie, le pipeline ne tronque pas les exemples, et les attributs **MF \_ TOPONODE \_ Mark \_ ici** et **MF \_ TOPONODE \_ MARKOUT \_ ici** sont ignorés. Si l’attribut n’est pas défini, ou a la valeur **false**, le pipeline tronque les exemples.

Une application peut définir l’attribut MARKOUT de la **\_ topologie MF \_ no \_ Mark \_** by sur **true** si l’application reçoit des exemples compressés du pipeline et doit recevoir toutes les images clés, qui peuvent être tronquées.

La valeur par défaut de cet attribut est **false**.

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

[**\_Mark MF TOPONODE \_ \_ ici**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**\_MARKOUT TOPONODE \_ MF \_ ici**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




