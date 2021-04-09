---
description: Un &\# 0034 ; contexte d’entrée&\# 0034 ; est une structure interne gérée par le IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contexte d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f1f83a397373e17a7d637b61a3232a3d72acde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864881"
---
# <a name="input-context"></a>Contexte d’entrée

Un « contexte d’entrée » est une structure interne gérée par le IMM. Elle contient des informations sur l’état de l’IME et est utilisée par les fenêtres IME. Par défaut, le système d’exploitation crée et assigne un contexte d’entrée à chaque thread. Dans le thread, ce contexte d’entrée par défaut est une ressource partagée et est associé à chaque nouvelle fenêtre créée.

Pour récupérer ou définir des informations dans l’IME, une application qui prend en charge l’IME doit d’abord récupérer un handle vers le contexte d’entrée associé à une fenêtre spécifiée. L’application récupère le descripteur à l’aide de la fonction [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) . Elle peut utiliser le handle récupéré dans les appels ultérieurs aux fonctions IMM pour récupérer et définir des valeurs IME, telles que le style de la fenêtre de composition, le style de composition et la position de la fenêtre d’État. Une fois que l’application a terminé d’utiliser le contexte, elle doit libérer le contexte à l’aide de la fonction [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) .

Étant donné que le contexte d’entrée par défaut est une ressource partagée, toute modification apportée par l’application s’applique à toutes les fenêtres du thread. Toutefois, l’application peut remplacer ce comportement par défaut en créant son propre contexte d’entrée et en l’associant à une ou plusieurs fenêtres du thread. Les modifications apportées à un contexte d’entrée spécifique à l’application s’appliquent uniquement aux fenêtres associées au contexte.

Votre application peut créer un contexte d’entrée à l’aide de la fonction [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) . Pour affecter le contexte à une fenêtre, l’application appelle la fonction [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . Cette fonction retourne un handle vers le contexte d’entrée associé précédemment. Si l’application n’a pas encore associé de contexte d’entrée à la fenêtre, le handle retourné correspond au contexte d’entrée par défaut. En règle générale, l’application enregistre ce handle et le réassocie ultérieurement à la fenêtre lorsque le contexte d’entrée personnalisé n’est plus nécessaire.

Une fois qu’un contexte d’entrée est associé à une fenêtre, le système d’exploitation sélectionne automatiquement ce contexte quand la fenêtre est activée et reçoit le focus d’entrée. Le style et d’autres informations dans le contexte d’entrée affectent l’entrée au clavier suivante pour cette fenêtre, en déterminant le fonctionnement de l’IME.

Votre application doit détruire tout contexte d’entrée personnalisé avant qu’elle ne se termine. Tout d’abord, l’application supprime le contexte d’entrée de toute association qu’il a faite avec Windows dans le thread à l’aide de la fonction [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . Ensuite, il appelle la fonction [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 



