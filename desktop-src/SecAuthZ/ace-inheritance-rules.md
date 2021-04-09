---
description: Le système propage les entrées de contrôle d’accès (ACE) pouvant être héritées aux objets enfants en fonction d’un ensemble de règles d’héritage.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Règles d’héritage ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8c786ebcc8450e8e5da1833f34fc85c37ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756196"
---
# <a name="ace-inheritance-rules"></a>Règles d’héritage ACE

Le système propage les entrées de [*contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) pouvant être héritées aux objets enfants en fonction d’un ensemble de règles d’héritage. Le système place les ACE héritées dans la liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) de l’enfant en fonction de l’ordre par défaut des entrées de contrôle d’accès [dans une liste DACL](order-of-aces-in-a-dacl.md). Le système définit l' \_ indicateur ACE hérité dans toutes les entrées du contrôle d’accès héritées.

Les ACE héritées par le conteneur et les objets enfants sans relation contenant-contenu diffèrent selon les combinaisons d’indicateurs d’héritage. Ces règles d’héritage fonctionnent de la même façon pour les DACL et les [*listes de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).



| Indicateur ACE parent                                  | Effet sur les listes de contrôle d’accès enfants                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L’objet \_ n’hérite que de l' \_ ACE                        | Objets enfants sans relation contenant-contenu : hérité comme ACE effectif. Objets enfants du conteneur : les conteneurs héritent d’une entrée du contrôle d’accès uniquement si l’indicateur de bit d’héritage de l' \_ ACE no Propagate \_ \_ est également défini.<br/>                                       |
| Hériter de l’ACE du conteneur \_ \_ uniquement                     | Objets enfants sans relation contenant-contenu : aucun effet sur l’objet enfant. Objets enfants du conteneur : l’objet enfant hérite d’une entrée du contrôle d’accès effective. L’entrée du contrôle d’accès héritée peut être héritée sauf si l’indicateur de bit d’héritage de l' \_ ACE no Propagate \_ \_ est également défini.<br/> |
| ACE \_ inherit conteneur \_ ACE et Object \_ inherit \_ ACE | Objets enfants sans relation contenant-contenu : hérité comme ACE effectif. Objets enfants du conteneur : l’objet enfant hérite d’une entrée du contrôle d’accès effective. L’entrée du contrôle d’accès héritée peut être héritée sauf si l’indicateur de bit d’héritage de l' \_ ACE no Propagate \_ \_ est également défini.<br/> |
| Aucun indicateur d’héritage défini                         | Aucun effet sur les objets conteneurs enfants ou non-conteneurs.                                                                                                                                                                                    |



 

Si une entrée du contrôle d’accès héritée est une entrée de contrôle d’accès effective pour l’objet enfant, le système mappe tous les droits génériques aux droits spécifiques pour l’objet enfant. De même, le système mappe les [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) génériques, tels que \_ le Créateur propriétaire, au SID approprié. Si une entrée du contrôle d’accès héritée est une entrée de contrôle d’accès en héritage uniquement, tous les droits génériques ou les SID génériques restent inchangés afin qu’ils puissent être mappés de manière appropriée lorsque l’entrée du contrôle d’accès est héritée par la nouvelle génération d’objets enfants.

Dans le cas où un objet conteneur hérite d’une entrée du contrôle d’accès qui est à la fois effective sur le conteneur et pouvant être héritée par ses descendants, le conteneur peut hériter de deux ACE. Cela se produit si l’entrée du contrôle d’accès héritable contient des informations génériques. Le conteneur hérite d’une entrée du contrôle d’accès qui contient les informations génériques et une entrée de contrôle d’accès (ACE) effective dans laquelle les informations génériques ont été mappées.

Une [entrée](object-specific-aces.md) du contrôle d’accès spécifique à un objet a un membre **InheritedObjectType** qui peut contenir un GUID pour identifier le type d’objet qui peut HÉRITer de l’entrée du contrôle d’accès.

Si le GUID **InheritedObjectType** n’est pas spécifié, les règles d’héritage pour une entrée du contrôle d’accès spécifique à un objet sont les mêmes que pour une entrée du contrôle d’accès standard.

Si le GUID **InheritedObjectType** est spécifié, l’entrée du contrôle d’accès peut être héritée par les objets qui correspondent au GUID si l’entrée du contrôle \_ d’accès \_ est définie par l’objet et par les conteneurs qui correspondent au GUID si le conteneur hérite de l’entrée de contrôle d’accès \_ \_ . Notez que actuellement, seuls les objets DS prennent en charge les ACE spécifiques aux objets, et le service d’annuaire traite tous les types d’objets en tant que conteneurs.

 

