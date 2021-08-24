---
title: Méthodes IPaper
description: Fournit des objets de copapiers qui sont contrôlés principalement par leur interface IPaper native.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a45322e35f07a6f136e76ecaad6ae237891a741dfb44a6b5db0702c87bda33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662719"
---
# <a name="ipaper-methods"></a>Méthodes IPaper

**StoServe** fournit des objets de copapier contrôlés principalement par leur interface **IPaper** native.

Le tableau suivant répertorie les méthodes **IPaper** à partir de IPaper. H dans le \\ répertoire frère Inc.



| Méthode    | Description                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Initialise l’objet Paper et crée un tableau de données d’encre.                 |
| Verrouillage      | Permet au client de contrôler le papier et de verrouiller les autres clients.      |
| Déverrouiller    | Abandonne le contrôle client du papier.                           |
| Load      | Charge le contenu papier à partir du fichier composé du client et avertit les récepteurs. |
| Enregistrer      | Enregistre le contenu du document dans le fichier composé du client.                      |
| InkStart  | Démarre le dessin de l’encre couleur sur l’aire du papier.                      |
| InkDraw   | Place des points de données d’encre sur la surface du papier électronique.               |
| InkStop   | Arrête le dessin manuscrit sur l’aire de papier.                             |
| Effacer     | Effacer le contenu du document actuel et avertit les récepteurs.                 |
| Redimensionner    | Redimensionne la taille du rectangle de dessin du papier et notifie les récepteurs.        |
| Redessiner    | Redessine le contenu de l’objet Paper et avertit les récepteurs.                |



 

Les méthodes intéressantes pour cet exemple de code sur les fichiers composés sont [**charger**](ipaper--load.md), [**Enregistrer**](ipaper--save.md)et [**redessiner**](ipaper--redraw.md).

[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) sont des méthodes utilisées par les clients pour enregistrer les séquences de dessin de l’encre. Le client répond généralement à un message WM \_ LBUTTONDOWN au début d’une séquence de dessin d’encre en appelant **InkStart** sur le codocument. Lorsque l’utilisateur déplace la souris ou le stylet pour dessiner tout en maintenant le bouton gauche enfoncé, le client répond aux \_ messages WM MOUSEMOVE répétés avec les appels correspondants à **InkDraw**. Quand l’utilisateur relâche le bouton gauche de la souris, le client répond à un \_ message WM LBUTTONUP avec un appel à **InkStop**, qui marque la fin de la séquence de dessin de l’encre.

[**InkStart**](inkstart-method.md) indique au codocument la position de début de la séquence de dessin dans les coordonnées de la fenêtre cliente. Il passe également la couleur et la largeur de l’encre actuellement sélectionnées. Le client gère ces sélections ; Le « colivre » les enregistre simplement lorsque l’appel **InkStart** est effectué. [**InkDraw**](inkdraw-method.md) est appelé à plusieurs reprises pour indiquer au codocument la succession des coordonnées de la fenêtre qui représentent le mouvement de dessin de la souris ou du stylet. [**InkStop**](cguipaper-methods.md) indique au codocument de marquer la fin d’une séquence de dessin.

 

 




