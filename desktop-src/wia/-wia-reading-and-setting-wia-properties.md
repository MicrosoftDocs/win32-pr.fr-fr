---
description: L’interface IWiaPropertyStorage fournit des méthodes pour lire et écrire les propriétés d’un élément WIA (Windows Image Acquisition). Les propriétés d’élément incluent les commandes d’appareil, les informations de format d’élément et les informations de périphérique.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lecture et définition des propriétés WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113286"
---
# <a name="reading-and-setting-wia-properties"></a>Lecture et définition des propriétés WIA

L’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fournit des méthodes pour lire et écrire les propriétés d’un élément WIA (Windows Image Acquisition). Les propriétés d’élément incluent les commandes d’appareil, les informations de format d’élément et les informations de périphérique.

Une application peut obtenir un pointeur vers une interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) d’un élément en énumérant les informations d’appareil ou les informations d’événement de l’élément en appelant [**IWiaItem :: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem :: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou en interrogeant l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) de l’élément. (Dans WIA 2,0, faites-le en appelant [**IWiaItem2 :: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) ou [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) ou en interrogeant l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément.)

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) hérite de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) et les méthodes héritées sont implémentées comme décrit dans la section de référence de stockage structuré dans le kit de développement logiciel (SDK) Windows.

> [!Note]
>
> Les applications WIA doivent toujours lire les en-têtes de données image pour obtenir des informations d’image précises. Le pilote WIA peut modifier les propriétés WIA et les en-têtes de données d’image pendant le transfert de données.
>
> Si aucun en-tête de données image n’est fourni avec le format spécifié, l’application WIA doit utiliser les propriétés WIA comme source d’informations sur le transfert de données. L’application WIA doit relire les propriétés WIA nécessaires une fois l’analyse ou la capture terminée pour obtenir les paramètres mis à jour.

 

Les sections suivantes décrivent les différentes propriétés WIA :

-   [Validation de la propriété WIA](-wia-wia-property-validation.md)
-   [Propriétés des informations sur l’appareil](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Propriétés de l’appareil](-wia-device-properties.md)
-   [Propriétés d'élément](-wia-item-properties.md)
-   [Propriétés WIA supplémentaires](-wia-additional-wia-properties.md)
-   [Définition des propriétés personnalisées](-wia-defining-custom-properties.md)
-   [Utilisation de propriétés personnalisées](-wia-using-custom-properties.md)
-   [Analyser le schéma de profil](-wia-scan-profile-schema.md)

 

 
