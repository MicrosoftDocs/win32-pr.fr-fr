---
title: Codes d’erreur de l’appareil
description: Les méthodes InvokeAction et QueryStateVariable retournent des valeurs HRESULT qui peuvent indiquer une erreur d’appareil (autrement dit, une erreur reçue d’un périphérique certifié UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463858"
---
# <a name="device-error-codes"></a>Codes d’erreur de l’appareil

Les méthodes [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) et [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) retournent des valeurs **HRESULT** qui peuvent indiquer une erreur d’appareil (autrement dit, une erreur reçue d’un périphérique certifié UPnP). Si une erreur est reçue à partir d’un appareil, la méthode ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ou [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) retourne une valeur **HRESULT** basée sur le code d’erreur de l’appareil, comme expliqué dans cette rubrique. Étant donné qu’une conversion est appliquée au code d’erreur de l’appareil pour produire une valeur **HRESULT** , vous ne pouvez pas lire le code d’erreur de l’appareil directement à partir de la valeur **HRESULT** .

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>Conversion d’un code d’erreur d’appareil en HRESULT

Il existe des codes d’erreur d’appareil standard et non standard. Les codes standard ont la même signification sur tous les appareils certifiés UPnP et ont des valeurs inférieures à 600. Les codes non standard sont spécifiques au fournisseur et ont des valeurs comprises entre 600 et 899.

Si le code d’erreur de l’appareil est standard ou non, détermine la façon dont la valeur **HRESULT** est générée :

-   Un code d’erreur d’appareil standard est mappé à une valeur **HRESULT** .

<!-- -->

-   Un code d’erreur d’appareil non standard est incorporé dans la valeur **HRESULT** en appliquant une formule.

Ces deux procédures peuvent être inversées pour déterminer le code d’erreur de l’appareil à partir d’une valeur **HRESULT** particulière.

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>Dérivation d’un code d’erreur d’appareil à partir d’une valeur HRESULT

Si la valeur **HRESULT** est supérieure ou égale à la **\_ \_ \_ \_ base spécifique d’action UPnP e** (0x80040300) et inférieure ou égale à la valeur **\_ \_ spécifique d’action \_ \_ e** (0x8004042B), le code d’erreur de l’appareil est non standard. Utilisez la formule de la section suivante pour déterminer le code d’erreur. Dans le cas contraire, le code d’erreur de l’appareil est standard : utilisez le tableau de la section mappage pour les codes d’erreur de l’appareil standard, qui fournit le mappage de la valeur **HRESULT** au code d’erreur de l’appareil.

Pour obtenir une description textuelle de l’erreur après un appel à [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), définissez le paramètre *pvarRetVal* sur un tableau vide. Lors du retour, ce paramètre contient une description textuelle de l’erreur, le cas échéant.

### <a name="formula-for-nonstandard-device-error-codes"></a>Formule pour les codes d’erreur d’appareil non standard

Utilisez la formule suivante si le plug-in de **\_ \_ \_ \_ base spécifique à une action UPnP e** **≤ ≤ valeur** d'**\_ action UPnP e \_ \_ \_ Max**.

Code d’erreur de l’appareil = (**HRESULT** de la  -  **\_ \_ \_ \_ base spécifique de l’action E**) + **\_ \_ \_ base spécifique** à l’action d’erreur

En remplaçant les valeurs numériques réelles, l’équation est : code d’erreur de l’appareil = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>Mappage pour les codes d’erreur d’appareil standard

Utilisez le mappage suivant si la  <  **\_ \_ \_ \_ base spécifique de l’action UPnP E** de HRESULT.



| Valeur HRESULT                    | Code d’erreur de l’appareil                | Valeur réelle |
|----------------------------------|----------------------------------|--------------|
| \_ \_ action non valide UPnP E \_         | \_action non valide d’erreur \_           | 401          |
| UPNP \_ E \_ arguments non valides \_      | \_argument Fault non valide \_              | 402          |
| UPNP \_ E \_ non \_ \_ synchronisé           | Numéro de séquence d’erreur \_ non valide \_ \_ | 403          |
| UPNP \_ E \_ variable non valide \_       | VARIABLE d’erreur \_ non valide \_         | 404          |
| échec de la demande d’action UPNP \_ E \_ \_ \_ | \_ \_ erreur interne du périphérique défaillant \_   | 501          |



 

## <a name="more-information"></a>Informations complémentaires

Les codes d’erreur de l’appareil sont spécifiés dans l' [architecture d’appareil UPnP version 1,0](https://openconnectivity.org/resources/documents.asp). Les constantes mentionnées dans cette rubrique sont définies dans les fichiers UPnP. h et UPnP. idl.

 

 




