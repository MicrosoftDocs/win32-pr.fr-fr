---
title: Opérations de Access Control et de lecture
description: La sécurité est un filtre implicite pour la recherche, l’énumération des conteneurs ou la lecture des propriétés.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Opérations de Access Control et de lecture AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028513"
---
# <a name="access-control-and-read-operations"></a>Opérations de Access Control et de lecture

La sécurité est un filtre implicite pour la recherche, l’énumération des conteneurs ou la lecture des propriétés. Si vous ne disposez pas des droits d’accès nécessaires, les tentatives d’énumération des objets ou de lecture des propriétés peuvent échouer avec les codes d’erreur suivants, même si l’objet ou la propriété existe :

-   **\_objet domaine E ADS \_ non valide \_ \_**
-   **\_propriété E \_ ADS \_ non \_ prise en charge**
-   **\_propriété ADS \_ E \_ \_ introuvable**

N’oubliez pas qu’un appelant avec des **publicités appropriées à la \_ \_ \_ liste ACTRL DS \_ List** pour un conteneur peut énumérer les objets enfants dans le conteneur. Toutefois, une tentative d’accès à un objet enfant peut encore échouer avec une erreur telle que **E \_ ADS \_ \_ objet inconnu** si l’appelant n’a pas d' **\_ \_ objet de \_ \_ liste \_ ACTRL DS** pour accéder à l’objet enfant.

L’impact de la sécurité sur les opérations de lecture n’est pas nécessairement représenté par une erreur. Par exemple, une opération de recherche peut être effectuée, mais les résultats de la recherche n’incluent pas les objets ou les propriétés auxquels l’appelant n’a pas accès.

 

 




