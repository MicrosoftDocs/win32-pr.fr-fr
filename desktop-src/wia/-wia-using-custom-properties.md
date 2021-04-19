---
description: Utilisation des propriétés personnalisées.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Utilisation de propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517524"
---
# <a name="using-custom-properties"></a>Utilisation de propriétés personnalisées

**Utilisation des propriétés personnalisées**.

Un pilote WIA (Windows Image Acquisition) peut définir ses propres propriétés personnalisées. Les appelants peuvent manipuler des propriétés personnalisées de la même façon que les propriétés WIA normales. Toutefois, seul votre application ou votre module d’interface utilisateur personnalisé peuvent accéder à ces propriétés personnalisées.

Les pilotes WIA doivent définir les propriétés personnalisées de façon à ce qu’elles aient des identificateurs de propriété qui sont décalées par les \_ DEVPROP privées WIA \_ pour les propriétés de l’appareil, et utiliser \_ \_ des ITEMPROP privées WIA pour les propriétés d’élément normales, par exemple dans [IWiaMiniDrv ::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx). Pour plus d’informations, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).

Il existe deux façons de passer des paramètres personnalisés à des pilotes WIA.

La première option consiste à utiliser la méthode **IWiaItemExtras :: Escape** (décrite dans la documentation du kit de développement logiciel (SDK) Platform). Cela est similaire à la méthode [IStiUSD :: Escape](https://msdn.microsoft.com/library/ms794396.aspx) , mais permet aux appelants d’utiliser WIA directement, au lieu d’utiliser les méthodes STI. À l’aide de **IWiaItemExtras :: Escape**, vous pouvez transmettre n’importe quelle information au pilote et le pilote peut transférer toutes les informations. Le service WIA gère uniquement les mémoires tampons transmises entre l’appelant et le pilote.

La deuxième option consiste à utiliser des propriétés personnalisées. L’utilisation de la méthode **IWiaItemExtras :: Escape** est plus souple que l’utilisation de propriétés WIA personnalisées, mais les propriétés WIA personnalisées vous permettent de stocker des informations dans le flux de propriété de l’élément afin que le pilote puisse lire les informations à un autre moment.

 

 



