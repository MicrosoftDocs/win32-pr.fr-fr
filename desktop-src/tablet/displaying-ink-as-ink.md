---
description: Le comportement par défaut du contrôle InkEdit consiste à reconnaître et convertir l’encre en texte après l’expiration d’un bref délai d’attente.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Affichage de l’encre sous forme d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518856"
---
# <a name="displaying-ink-as-ink"></a>Affichage de l’encre sous forme d’encre

Le comportement par défaut du contrôle [InkEdit](inkedit-control-reference.md) consiste à reconnaître et convertir l’encre en texte après l’expiration d’un bref délai d’attente. Étant donné que le contrôle est une superclasse de [RichEdit](../controls/rich-edit-controls.md), il est également possible d’incorporer et d’afficher de l’encre dans le contrôle. Chaque mot est inséré dans le contrôle en tant qu’objet [**InkDisp**](inkdisp-class.md) . L’objet **InkDisp** contient l’encre et ses alternatives de reconnaissance.

Lorsqu’elle est insérée, l’encre est mise à l’échelle en fonction de la taille de police actuelle et d’autres propriétés ambiantes, telles que l’italique ou le gras, sont appliquées. Si l’utilisateur choisit de modifier le texte d’un objet [**InkDisp**](inkdisp-class.md) , il doit d’abord convertir l’entrée manuscrite en texte.

> [!Note]  
> Toutes les autres données d’encre et de reconnaissance sont perdues lors de la conversion.

 

Cette fonctionnalité est disponible uniquement sur les ordinateurs qui exécutent Microsoft Windows XP Édition Tablet PC, Windows Vista ou version ultérieure.

 

 
