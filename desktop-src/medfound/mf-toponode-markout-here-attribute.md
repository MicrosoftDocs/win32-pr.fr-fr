---
description: Spécifie si le pipeline applique le marquage sur ce nœud. Le marquage est l’endroit où se termine une présentation. Si les composants de pipeline génèrent des données au-delà du point de marquage, les données ne sont pas rendues.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Attribut MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519770"
---
# <a name="mf_toponode_markout_here-attribute"></a>\_TOPONODE MF \_ MARKOUT \_ ici, attribut

Spécifie si le pipeline applique le marquage sur ce nœud. Le marquage est l’endroit où se termine une présentation. Si les composants de pipeline génèrent des données au-delà du point de marquage, les données ne sont pas rendues.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut s’applique à tous les types de nœuds.

Si cet attribut a la **valeur true**, le pipeline Media Foundation supprime les exemples de sortie de ce nœud pour qu’ils correspondent à l’heure d’arrêt de la présentation. Le chargeur de topologie définit cet attribut lorsqu’il résout une topologie. La plupart des applications n’ont pas besoin de définir ou de récupérer cet attribut.

Il est recommandé que cet attribut soit défini sur **true** pour chaque branche de la topologie. Une branche de topologie est définie en tant que chemin d’accès d’un nœud source à un nœud de sortie. Au sein d’une branche, \_ les \_ attributs MF TOPONODE MARKOUT \_ ici et [MF \_ TOPONODE \_ Mark \_ here](mf-toponode-markin-here-attribute.md) doivent être définis sur le même nœud dans la branche. Ils ne peuvent pas être définis sur des nœuds différents dans la même branche.

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

[**\_Mark MF TOPONODE \_ \_ ici**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




