---
description: Spécifie si une Media Foundation transformation (MFT) est inscrite uniquement dans le processus d’application.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Attribut MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753941"
---
# <a name="mft_process_local_attribute-attribute"></a>Attribut de l' \_ \_ attribut local du processus MFT \_

Spécifie si une Media Foundation transformation (MFT) est inscrite uniquement dans le processus de l’application.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut est utilisé comme suit :

1.  L’application inscrit une table MFT locale en appelant la fonction [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) . Ces fonctions inscrivent la table MFT dans le processus de l’application.
2.  La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) est appelée pour énumérer les MFTS qui correspondent à un ensemble de critères particulier. L’application peut appeler la fonction **MFTEnumEx** directement, mais cette fonction est plus souvent appelée par le chargeur de topologie.
3.  La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) récupère un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , chacun représentant un objet d’activation pour une table MFT. Si une table MFT est inscrite localement, l’attribut de l' \_ attribut local de processus MFT a la valeur \_ \_ **true** sur l’objet d’activation correspondant.

La valeur par défaut de cet attribut est **false**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




