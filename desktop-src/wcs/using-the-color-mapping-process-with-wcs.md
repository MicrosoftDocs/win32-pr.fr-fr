---
title: Utilisation du processus de mappage des couleurs avec WCS
description: Le mappage des couleurs WCS est basé sur les profils d’appareil.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Système de couleurs (WCS), mappage des couleurs
- WCS (Windows color System), mappage des couleurs
- gestion des couleurs des images, mappage des couleurs
- gestion des couleurs, mappage des couleurs
- couleurs, mappage des couleurs
- mappage des couleurs
- Windows Système de couleurs (WCS), profils d’appareil
- WCS (Windows Color System), profils d’appareil
- gestion des couleurs des images, profils d’appareil
- gestion des couleurs, profils d’appareil
- couleurs, profils d’appareil
- Windows Système de couleurs (WCS), profils
- WCS (Windows Color System), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- profils d’appareil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe785af9fa4160c2aa1e54c6765857edc9c7aacb1a8fa40a0ad04e634b4ab602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934259"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Utilisation du processus de mappage des couleurs avec WCS

Le mappage des couleurs WCS est basé sur les [profils d’appareil](d.md). Ils sont fournis par les fournisseurs de périphériques matériels en couleurs et installés lors de l’installation d’un appareil. Lorsque le mappage des couleurs est utilisé par un programme d’application, WCS accède au profil d’appareil de l’image pour récupérer les informations nécessaires à la conversion de l’image en PC. La conversion est effectuée par le CMM.

Un profil d’appareil peut être incorporé dans l’image elle-même. Le profil d’appareil est donc parcouru avec l’image, même sur Internet. Un utilisateur n’a pas besoin de l’appareil source pour obtenir un mappage de couleurs précis. Si une image n’a pas de profil d’appareil, l’espace sRVB est utilisé comme valeur par défaut. Pour plus d’informations, consultez [utilisation de la gestion des couleurs sur Internet](using-color-management-on-the-internet.md).

Notez que les applications qui utilisent WCS ne doivent jamais incorporer le profil sRVB dans une image. L’espace colorimétrique sRVB fournit un espace de couleurs standardisé qui est portable sur tous les appareils. elle est automatiquement disponible pour les utilisateurs de Windows 98 et versions ultérieures, ainsi que Windows 2000 et versions ultérieures. Par conséquent, il n’est pas nécessaire de voyager avec l’image.

Une fois que les couleurs de l’image se trouvent dans les [PC](p.md), WCS accède au profil d’appareil de l’appareil de destination. Il obtient le CMM pour convertir les couleurs d’image des PC en gamme de l’appareil de destination.

Un mappage de couleurs plus complexe peut également être effectué à l’aide du WCS. Par exemple, il peut être utilisé pour obtenir une idée de ce à quoi ressemble une image créée sur un écran vidéo lorsqu’elle est imprimée sur une imprimante laser haute résolution. L’exemple devient plus complexe s’il n’existe qu’une imprimante à jet d’encre standard sur laquelle le prévisualiser. L’image peut être convertie à partir de la gamme de l’affichage, dans la gamme de l’imprimante à jet d’encre. À partir de là, il peut être converti en gamme de l’imprimante laser. L’image résultante peut être imprimée sur l’imprimante à jet d’encre. Bien sûr, l’image serait à une résolution plus élevée lorsqu’elle est imprimée sur l’imprimante laser couleur. Toutefois, les couleurs de l’image de vérification imprimée sur l’imprimante à jet d’encre sont une correspondance proche des couleurs que l’imprimante laser peut imprimer.

La façon dont les conversions dans l’exemple sont effectuées consiste à convertir les couleurs de l’image de la gamme de l’affichage en PC. Une fois les couleurs d’image converties en PC, le profil d’appareil de l’imprimante à jet d’encre est utilisé pour les transformer en couleurs de l’imprimante à jet d’encre. Ensuite, la transformation gamme à PC est utilisée pour ramener les couleurs aux PC. À partir de là, le profil d’appareil de l’imprimante laser est utilisé pour convertir les couleurs des PC dans la gamme de l’imprimante laser.

La possibilité de transformer facilement les couleurs d’une gamme d’appareils en ordinateurs, puis de nouveau, permet de vérifier les couleurs d’image destinées à un appareil de sortie en couleur sur pratiquement tous les autres.

Dans l’exemple précédent, la description est légèrement différente de la procédure réelle pour plus de clarté. En réalité, toutes les transformations mentionnées dans le paragraphe précédent sont concaténées en une seule transformation.

 

 




