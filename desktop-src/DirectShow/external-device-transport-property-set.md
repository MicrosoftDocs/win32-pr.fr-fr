---
description: Ensemble de propriétés de transport d’appareil externe
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Ensemble de propriétés de transport d’appareil externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224500"
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

 

 



