---
title: Couche de débogage Direct2D
description: Extension d’exécution pour Direct2D qui fournit des messages d’erreur descriptifs, la détection des fuites d’objets, des notifications de performances et d’autres signaux pour vous aider à créer des applications Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113285"
---
# <a name="direct2d-debug-layer"></a>Couche de débogage Direct2D

## <a name="purpose"></a>Objectif

La couche de débogage Direct2D, implémentée séparément de Direct2D dans sa propre DLL nommée d2d1debug.dll, fournit des messages de débogage au moment du design pour réduire l’échec de l’application Runtime. Les messages de débogage résultent souvent de violations de contrats d’API telles que les paramètres non valides (qui peuvent être liés à Direct3D), de ressources non valides, de violations de threads et d’autres problèmes de performances, tels que l’utilisation d’une couche quand un clip suffit.

Pour vous aider à déterminer la quantité d’informations qui est tracée par la couche de débogage, la couche de débogage offre trois niveaux de débogage : informations, avertissement et erreur. Ces trois niveaux sont interprétés comme suit :

-   **Erreur :** Direct2D envoie des messages d’erreur graves à la couche de débogage. Par exemple, l’interruption d’une contrainte de thread génère une erreur grave.

    En outre, un message d’erreur de niveau déclenche le point d’arrêt pour vous aider à effectuer le débogage.

-   **Avertissement :** Direct2D envoie des messages d’erreur et des avertissements à la couche de débogage pour vous permettre de traiter l’un de ces messages.

-   **Informations :** Direct2D envoie des messages d’erreur, des avertissements et des informations de diagnostic supplémentaires à la couche de débogage. Par exemple, les messages d’amélioration des performances seront envoyés à ce niveau de débogage.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Installation de la couche de débogage Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Décrit comment installer la couche de débogage Direct2D.<br/>      |
| [Vue d’ensemble de la couche de débogage Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Messages de débogage](direct2ddebuglayer-debugmessages.md)<br/>                         | Répertorie les messages de débogage de la couche de débogage Direct2D.<br/> |



 

 

 





