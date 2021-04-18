---
description: Spécifie si le fournisseur de captures vocales stocke les statistiques de datage dans le registre.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533783"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ récupérer \_ les \_ statistiques TS, propriété

Spécifie si le fournisseur de captures vocales stocke les statistiques de datage dans le registre.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ false

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

Les algorithmes d’annulation de l’écho acoustique (AEC) dépendent des horodatages précis des flux audio. En réalité, les horodatages sont souvent imparfaits, et différents périphériques audio peuvent présenter des taux de variance et de dérive différents. Lorsque l’AEC est activé, le DSP collecte des statistiques sur les horodatages et utilise ces informations pour compenser les imprécisions.

Si la valeur de cette propriété est \_ true, le DSP enregistre les statistiques qu’il collecte dans le registre. La prochaine fois que le DSP effectue l’AEC à l’aide de la même paire de périphériques audio, il lit les informations statistiques du Registre, ce qui permet au DSP de s’exécuter plus efficacement.

Si vous affectez à cette propriété la valeur VARIANT \_ true et que vous utilisez le DSP en mode filtre, vous devez également définir la propriété [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) . En mode Source, ce n’est pas obligatoire.

La valeur par défaut de cette propriété est \_ false false. Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
