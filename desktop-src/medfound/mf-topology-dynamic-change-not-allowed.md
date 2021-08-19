---
description: Spécifie si la session multimédia tente de modifier la topologie lorsque le format d’un flux de contenu change.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Attribut MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2e984b45abc55246c9b1ae291c535c7fbb00f01f9405d827b7fe833b57a368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875728"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>\_Attribut modification dynamique de la topologie MF \_ \_ \_ non \_ autorisé

Spécifie si la session multimédia tente de modifier la topologie lorsque le format d’un flux de contenu change.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarques

Cet attribut contrôle la manière dont la session multimédia répond si le format d’un flux est modifié pendant la diffusion en continu.

Si le format change et que l' \_ attribut modification dynamique de la topologie MF \_ \_ \_ n' \_ est pas autorisé a la **valeur false**, la session multimédia peut insérer de nouveaux nœuds dans la topologie pour qu’ils correspondent au nouveau format. Par exemple, si la taille de la vidéo change, la session multimédia peut ajouter une transformation de Media Foundation (MFT) qui redimensionne la vidéo. Sinon, si l’attribut a la **valeur true**, la session multimédia ne modifiera pas la topologie.

La valeur par défaut de cet attribut est **false**. La valeur recommandée est **false**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




