---
title: Chargement du caractère par défaut
description: Chargement du caractère par défaut
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106529059"
---
# <a name="loading-the-default-character"></a>Chargement du caractère par défaut

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Au lieu de charger un caractère spécifique directement en spécifiant son nom de fichier, vous pouvez charger le *caractère par défaut*. Le caractère par défaut est un service destiné à fournir un Assistant Windows partagé et central que l’utilisateur choisit. Microsoft Agent comprend une feuille de propriétés dans le cadre du service de caractères par défaut, connu sous le nom de Fenêtre Propriétés de caractères, qui permet à l’utilisateur de modifier sa sélection du caractère par défaut.

La sélection du caractère par défaut est limitée à un caractère qui prend en charge le jeu d’animations standard, garantissant ainsi un niveau de cohérence de base entre les caractères. Cela n’exclut pas un caractère de l’existence d’animations supplémentaires.

Toutefois, étant donné que le caractère par défaut est destiné à une utilisation à usage général et peut être partagé par d’autres applications en même temps, évitez de charger le caractère par défaut lorsque vous souhaitez utiliser un caractère exclusivement pour votre application.

Pour charger le caractère par défaut, appelez la méthode [**Load**](load-method.md) sans spécifier de nom de fichier ou de chemin d’accès. Microsoft agent charge automatiquement le jeu de caractères actuel comme caractère par défaut. Si l’utilisateur n’a pas encore sélectionné un caractère par défaut, agent sélectionne le premier caractère qui prend en charge l’ensemble d’animations standard. Si aucun n’est disponible, la méthode échoue et signale la cause du problème.

Bien qu’une application cliente puisse se renseigner sur l’identité du caractère, seul un utilisateur peut modifier ses paramètres. Vous pouvez utiliser [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) pour afficher les fenêtre Propriétés de caractères.

Le serveur notifie les clients qui ont chargé le caractère par défaut lorsqu’un utilisateur modifie une sélection de caractères et transmet le GUID du nouveau caractère. Le serveur décharge automatiquement le premier caractère et recharge le nouveau caractère. Les files d’attente de tous les clients qui ont chargé le caractère par défaut sont arrêtées et vidées. Toutefois, les files d’attente des clients qui ont chargé le caractère explicitement à l’aide du nom de fichier du caractère ne sont pas affectées. Si nécessaire, le serveur gère également automatiquement la réinitialisation automatique du moteur TTS (Text-to-Speech) pour le nouveau caractère.

 

 




