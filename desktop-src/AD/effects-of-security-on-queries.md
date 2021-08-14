---
title: Effets de la sécurité sur la recherche
description: La sécurité est un filtre implicite lors de l’exécution de recherches, de l’énumération des conteneurs ou de la lecture des propriétés.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- effets de la sécurité sur la recherche Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191619"
---
# <a name="effects-of-security-on-searching"></a>Effets de la sécurité sur la recherche

La sécurité est un filtre implicite lors de l’exécution de recherches, de l’énumération des conteneurs ou de la lecture des propriétés.

ADSI ne peut retourner \_ aucune \_ propriété de ce type ou aucune \_ \_ erreur d’objet, même lorsque l’objet existe si vous n’avez pas accès à des attributs de lecture sur l’objet.

Par exemple, un appelant peut être en mesure d’énumérer les objets enfants dans un conteneur, car l’appelant a \_ des droits de liste de contenu sur le conteneur. Toutefois, il se peut que le même appelant ne puisse pas accéder aux objets énumérés si l’appelant n’a pas d’accès en lecture aux objets enfants. Dans ce cas, une requête pour un objet enfant peut retourner un \_ objet de ce type, \_ même si l’appelant a énuméré correctement l’objet.

Si l’appelant ne dispose pas de droits suffisants, les codes de retour suivants peuvent être retournés :

\_objet domaine E ADS \_ non valide \_ \_

\_propriété E \_ ADS \_ non \_ prise en charge

\_propriété ADS \_ E \_ \_ introuvable

 

 




