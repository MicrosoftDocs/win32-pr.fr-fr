---
description: Vue d’ensemble de la désignation d’une fenêtre de manière appropriée et de la définition de la légende de la fenêtre pour Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Attribution d’un nom à une fenêtre de manière appropriée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520057"
---
# <a name="naming-a-window-appropriately"></a>Attribution d’un nom à une fenêtre de manière appropriée

Assignez à chaque fenêtre une légende conviviale, même si la fenêtre ou sa légende est invisible. Cela permet à la fonctionnalité de reconnaissance vocale d’identifier la fenêtre et la hiérarchie de la fenêtre. Cette recommandation s’applique à toutes les fenêtres : les fenêtres de niveau supérieur avec des frames visibles. les fenêtres enfants, telles que les palettes flottantes ; contrôles personnalisés ; barres d’outils et les volets dans une fenêtre, lorsqu’ils sont implémentés en tant que fenêtres enfants.

Il existe trois façons de définir le titre de la fenêtre :

-   Définissez la chaîne dans votre script de ressources lors de l’appel de [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou de fonctions connexes.
-   Appelez la fonction [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .
-   Définissez le nom des contrôles dans les boîtes de dialogue à l’aide des techniques décrites dans la rubrique [nommer des contrôles dans les boîtes de dialogue](naming-controls-in-dialog-boxes.md). Il s’agit de la seule méthode pour étiqueter un contrôle d’édition, car la définition de l’étiquette intrinsèque Controls modifie le contenu des contrôles.

Vous pouvez interroger la légende à l’aide de l’Active Accessibility Microsoft ou du \_ message WM GETTEXT.

Pour plus d’informations sur l’interrogation de la légende à l’aide de Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) .

 

 
