---
description: Spécifie l’heure de début des présentations mises en file d’attente après la première présentation.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Attribut MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524079"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_ \_ Heure de début de la topologie MF \_ sur l' \_ \_ attribut de commutateur de présentation \_

Spécifie l’heure de début des présentations mises en file d’attente après la première présentation.

## <a name="data-type"></a>Type de données

**Int64** stocké comme **UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S'applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Notes

Lorsque l’application met en file d’attente la première présentation sur la session multimédia, l’application spécifie l’heure de début dans le paramètre *pvarStartPosition* de la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) . Toutefois, pour toutes les présentations ultérieures, l’heure de début est indiquée par l' \_ \_ heure de début de la topologie MF \_ \_ sur \_ \_ l’attribut de changement de présentation sur la topologie. L’heure de début est spécifiée en unités de 100 nanosecondes, par rapport au début de la présentation. Par exemple, si la valeur est 50 millions, la lecture démarre 5 secondes dans la présentation. Si cet attribut n’est pas défini, l’heure de début par défaut est zéro.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




