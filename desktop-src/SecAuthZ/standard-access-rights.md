---
description: Chaque type d’objet sécurisable possède un ensemble de droits d’accès qui correspondent à des opérations spécifiques à ce type d’objet.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Droits d’accès standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413469"
---
# <a name="standard-access-rights"></a>Droits d’accès standard

Chaque type d’objet sécurisable possède un ensemble de droits d’accès qui correspondent à des opérations spécifiques à ce type d’objet. En plus de ces droits d’accès spécifiques aux objets, il existe un ensemble de droits d’accès standard qui correspondent à des opérations communes à la plupart des types d’objets sécurisables.

Le [format de masque d’accès](access-mask-format.md) comprend un ensemble de bits pour les droits d’accès standard. les constantes d’Windows suivantes pour les droits d’accès standard sont définies dans winnt. h.



| Constante      | Signification                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suppression        | Droit de supprimer l'objet.                                                                                                                                                                                                                                                                                                              |
| LIRE \_ le contrôle | Droit de lire les informations du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet, à l’exclusion des informations contenues dans la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). |
| SYNCHRONIZE   | Droit d'utiliser l'objet pour la synchronisation. Cela permet à un thread d’attendre jusqu’à ce que l’objet soit dans l’état signalé. Certains types d’objets ne prennent pas en charge ce droit d’accès.                                                                                                                                                                |
| ÉCRITURE \_ DAC    | Droit de modifier la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) dans le descripteur de sécurité de l’objet.                                                                                                                    |
| propriétaire en écriture \_  | Droit de modifier le propriétaire défini dans le descripteur de sécurité de l'objet.                                                                                                                                                                                                                                                                           |



 

Winnt. h définit également les combinaisons suivantes des constantes de droits d’accès standard.



| Constante                   | Signification                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_droits standard \_ tous      | Combine la suppression, \_ le contrôle de lecture, \_ l’écriture DAC, le propriétaire d’écriture \_ et l’accès de synchronisation. |
| \_exécution des droits standard \_  | Actuellement défini en tant que contrôle de lecture égal \_ .                                         |
| \_droits de \_ lecture standard     | Actuellement défini en tant que contrôle de lecture égal \_ .                                         |
| \_droits standard \_ requis | Combine les accès de suppression, de \_ contrôle de lecture, d’écriture \_ DAC et de propriétaire d’écriture \_ .              |
| \_écriture des droits standard \_    | Actuellement défini en tant que contrôle de lecture égal \_ .                                         |



 

 

 
