---
title: Interaction avec WinEvents
description: L’heure d’exécution de l’annotation dynamique n’enverra pas de WinEvents ; Il incombe à l’annotation d’envoyer les événements appropriés, si nécessaire. Si vous devez envoyer des WinEvents, veillez à les envoyer une fois l’annotation effectuée.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098459"
---
# <a name="interaction-with-winevents"></a>Interaction avec WinEvents

L’heure d’exécution de l’annotation dynamique n’enverra pas de [winEvents](winevents-infrastructure.md); Il incombe à l’annotation d’envoyer les événements appropriés, si nécessaire. Si vous devez envoyer des WinEvents, veillez à les envoyer une fois l’annotation effectuée.

Par exemple, si vous utilisez [**IAccPropServices :: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) pour définir la propriété [**Name**](name-property.md) d’un élément, envoyez un [**événement \_ \_ NameChange, d’objet d’événement**](event-constants.md) pour cet objet après que **SetPropValue** a été retourné.

Toutefois, si vous utilisez [**IAccPropServices :: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) pour définir ValueMap pour un Slider, aucun événement n’est nécessaire, car la définition de ValueMap ne modifie pas la valeur du curseur.

 

 




