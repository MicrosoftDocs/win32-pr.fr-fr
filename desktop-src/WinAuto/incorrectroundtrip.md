---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197145"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texte

Appelez accNavigate ((cliquez sur répéter pour être rappelé dans :), 1, NAVDIR \_ suivant), puis accNavigate ((ouvrir), 2, NAVDIR \_ précédent). l’opération doit être retournée. cliquez sur répéter pour être rappelé dans : (childID = 1), mais retournée cliquez sur répéter pour être rappelé dans :

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

l’utilisation de [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) pour traverser l’arborescence d’éléments de la cible de vérification ne retourne pas le même élément de départ lorsque la direction de traversée est inversée.

![exemple d’implémentation MSAA non valide qui a provoqué une navigation aller-retour incorrecte](images/accchecker-invalid-round-trip.png)

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




