---
description: Ensemble de propriétés de transport d’appareil externe
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Ensemble de propriétés de transport d’appareil externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef7db31dfe80fae0178aa329ce7e3c6cd55d3a6acbef7fd5a8ccda07943bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685669"
---
# <a name="external-device-transport-property-set"></a>Ensemble de propriétés de transport d’appareil externe

Ce jeu de propriétés contrôle le transport des données vers et à partir d’un périphérique externe. Dans la plupart des cas, les applications ne doivent pas utiliser cette propriété directement définie. Utilisez plutôt l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .

Le tableau suivant répertorie les propriétés qui sont pertinentes pour les applications en mode utilisateur. pour obtenir une description complète de ce jeu de propriétés, reportez-vous au kit de développement de pilotes Microsoft Windows driver kit DDK.



| Étiquette | Valeur |
|-------------------|---------------------------|
| GUID de jeu de propriétés | \_transport PROPSETID ext \_ |



 



| ID de propriété                                                                           | Description                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**\_recherche KSPROPERTY EXTXPORT \_ ATN \_**](ksproperty-extxport-atn-search.md)           | Recherche un numéro de piste absolu (ATN). |
| [**\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_**](ksproperty-extxport-timecode-search.md) | Recherche un code d’heure.                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 



