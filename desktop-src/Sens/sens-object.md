---
description: Le service de notification d’événements système (SENS) définit la coclasse SENSe dans le cadre de la bibliothèque de types SENSe.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Objet SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013576"
---
# <a name="sens-object"></a>Objet SENS

Le service de notification d’événements système (SENS) définit la coclasse SENSe dans le cadre de la bibliothèque de types SENSe.

## <a name="implementation"></a>Implémentation

L’implémentation d’objet SENSe est fournie par le système d’exploitation.

## <a name="creationaccess-functions"></a>Fonctions de création et d’accès



| Fonction                                      | Description                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Crée une instance de l’objet SENS à l’aide de son CLSID. |



 

## <a name="interfaces"></a>Interfaces



| Interface                            | Description                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Par défaut. Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interface sortante implémentée par l’objet récepteur dans l’application de l’abonné. disponible avec Windows XP. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[À propos du service de notification d’événements système](about-system-event-notification-service.md)
</dt> </dl>

 

 
