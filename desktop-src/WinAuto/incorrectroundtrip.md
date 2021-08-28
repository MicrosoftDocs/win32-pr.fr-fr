---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644733"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texte

Appelez accNavigate ((cliquez sur répéter pour être rappelé dans :), 1, NAVDIR \_ suivant), puis accNavigate ((ouvrir), 2, NAVDIR \_ précédent). l’opération doit être retournée. cliquez sur répéter pour être rappelé dans : (childID = 1), mais retournée cliquez sur répéter pour être rappelé dans :

## <a name="type"></a>Type

Erreur

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

 

 




