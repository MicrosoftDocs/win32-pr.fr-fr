---
description: Ensemble de propriétés de transport d’appareil externe
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Ensemble de propriétés de transport d’appareil externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109902"
---
# <a name="external-device-transport-property-set"></a>Ensemble de propriétés de transport d’appareil externe

Ce jeu de propriétés contrôle le transport des données vers et à partir d’un périphérique externe. Dans la plupart des cas, les applications ne doivent pas utiliser cette propriété directement définie. Utilisez plutôt l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .

Le tableau suivant répertorie les propriétés qui sont pertinentes pour les applications en mode utilisateur. Pour obtenir une description complète de ce jeu de propriétés, reportez-vous au kit de développement de pilotes Microsoft Windows Driver kit DDK.



|                   |                           |
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

 

 



