---
description: La classe de fenêtre IME est une classe globale système prédéfinie qui définit l’apparence et le comportement des fenêtres IME standard.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe de fenêtre IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56449534467a2b01ce8e59991bfc1c5f5ad4e1a9156f86cee5e154a8b8eb1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107189"
---
# <a name="ime-window-class"></a>Classe de fenêtre IME

La classe de fenêtre IME est une classe globale système prédéfinie qui définit l’apparence et le comportement des fenêtres IME standard. La classe est semblable aux classes de contrôles communs dans le fait que l’application crée une fenêtre de cette classe à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . À l’instar des contrôles statiques, une fenêtre IME ne répond pas aux entrées d’utilisateur par elle-même. Au lieu de cela, il avertit l’IME des actions d’entrée d’utilisateur et traite les messages de contrôle qui lui sont envoyés par l’IME ou les applications pour effectuer une réponse à l’action de l’utilisateur.

Les applications prenant en charge l’IME créent parfois des fenêtres IME personnalisées à l’aide de la classe de fenêtre IME. L’utilisation de la personnalisation de fenêtre permet à l’application de tirer parti du traitement par défaut de la fenêtre IME tout en contrôlant le positionnement de la fenêtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 
