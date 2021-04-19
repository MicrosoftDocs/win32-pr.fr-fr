---
description: Spécifie si le pipeline applique la marque dans ce nœud.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Attribut MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545802"
---
# <a name="mf_toponode_markin_here-attribute"></a>\_ \_ Attribut Mark TOPONODE MF \_ ici

Spécifie si le pipeline applique la marque dans ce nœud. Mark-in est l’endroit où commence une présentation. Si les composants de pipeline génèrent des données avant le point de marque, les données ne sont pas rendues.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

> [!Note]  
> La plupart des applications n’ont pas besoin d’utiliser cet attribut. La [session multimédia](media-session.md) définit automatiquement cet attribut, si nécessaire.

 

Cet attribut s’applique à tous les types de nœuds. Si l’attribut a la **valeur true**, le pipeline Media Foundation supprime les exemples de sortie de ce nœud afin qu’il corresponde à l’heure de début de la présentation. Le chargeur de topologie définit cet attribut lorsqu’il résout une topologie.

Il est recommandé que cet attribut soit défini sur **true** pour chaque branche de la topologie. Une branche de topologie est définie en tant que chemin d’accès d’un nœud source à un nœud de sortie. Au sein d’une branche, les attributs [MF \_ TOPONODE \_ MARKOUT \_ ici](mf-toponode-markout-here-attribute.md) et MF \_ TOPONODE \_ Mark \_ here doivent être définis sur le même nœud dans la branche. Ils ne peuvent pas être définis sur des nœuds différents dans la même branche.

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

[**\_MARKOUT TOPONODE \_ MF \_ ici**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




