---
title: Valeurs de retour (fonctionnalités d’accessibilité Windows)
description: Cette rubrique décrit les valeurs de retour les plus courantes et les autres valeurs de retour que vous pouvez voir moins fréquemment.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443990"
---
# <a name="return-values-windows-accessibility-features"></a>Valeurs de retour (fonctionnalités d’accessibilité Windows)

Cette rubrique décrit les valeurs de retour les plus courantes et les autres valeurs de retour que vous pouvez voir moins fréquemment.

## <a name="common-return-values"></a>Valeurs de retour courantes

Les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retournent l’une des valeurs suivantes, définies dans Winerror. h, ou un autre code d’erreur com (Component Object Model) standard :



|   Value                      |   Description                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OK                   | S_OK                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ false                | La méthode a réussi en partie. Cela se produit lorsque la méthode est réussie, mais que les informations demandées ne sont pas disponibles. Par exemple, Microsoft Active Accessibility retourne S \_ false si vous appelez [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) pour récupérer un objet enfant à un point donné et que le point spécifié ne se trouve pas dans l’objet ou l’enfant de l’objet. |
| \_MEMBERNOTFOUND DISP \_ | L’objet ne prend pas en charge la propriété ou l’action demandée. Par exemple, un bouton de commande retourne cette valeur si vous demandez sa [propriété Value](value-property.md), car elle ne possède pas de propriété Value.                                                                                                                                                                           |
| \_NOTIMPL E              | Cette méthode n'est pas implémentée. Cette valeur se produit lorsqu’un client appelle une méthode qui n’est pas encore prise en charge dans ce système d’exploitation.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Un ou plusieurs arguments ne sont pas valides. Cette erreur se produit lorsque l’appelant tente d’identifier un objet enfant à l’aide d’un identificateur que le serveur ne reconnaît pas. Cette erreur se produit également lorsqu’un client tente d’identifier un objet enfant dans un objet qui n’a pas d’enfants.                                                                                                      |
| \_OUTOFMEMORY E          | La méthode n’a pas pu allouer de la mémoire requise pour terminer une opération cruciale pour sa réussite.                                                                                                                                                                                                                                                                                        |
| E \_ échec                 | Une erreur inconnue ou générique s’est produite.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valeurs de retour supplémentaires

Les valeurs de retour suivantes peuvent être retournées par les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Ces valeurs de retour ne sont pas aussi courantes que les valeurs précédentes, mais vous devez en être conscient.



|    Value                    |    Description                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| \_ACCESSDENIED E        | Elle est retournée lorsque vous appelez \_ la commande obtenir accValue pour obtenir la valeur d’un contrôle de mot de passe. |
| \_exception DISP E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




