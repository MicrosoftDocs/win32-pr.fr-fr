---
description: Un processus parent peut spécifier des propriétés associées à la fenêtre principale de son processus enfant.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Définition des propriétés des fenêtres à l’aide de STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637e8fc9c76694a468b4b8fa6d5d2bd8a3432bbb7dad078d616df753244af358
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517379"
---
# <a name="setting-window-properties-using-startupinfo"></a>Définition des propriétés des fenêtres à l’aide de STARTUPINFO

Un processus parent peut spécifier des propriétés associées à la fenêtre principale de son processus enfant. La fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) prend un pointeur vers une structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) comme l’un de ses paramètres. Utilisez les membres de cette structure pour spécifier les caractéristiques de la fenêtre principale du processus enfant. Le membre **dwFlags** contient un champ de binaire qui détermine les autres membres de la structure qui sont utilisés. Cela vous permet de spécifier des valeurs pour n’importe quel sous-ensemble des propriétés de la fenêtre. Le système utilise les valeurs par défaut pour les propriétés que vous ne spécifiez pas. Le membre **dwFlags** peut également forcer l’affichage d’un curseur de commentaires pendant l’initialisation du nouveau processus.

Pour les processus d’interface utilisateur graphique, la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) spécifie les valeurs par défaut à utiliser la première fois que le nouveau processus appelle les fonctions [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) et [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) pour créer et afficher une fenêtre Overlapped. Les valeurs par défaut suivantes peuvent être spécifiées :

-   Largeur et hauteur, en pixels, de la fenêtre créée par [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Emplacement, en coordonnées d’écran, de la fenêtre créée par [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Paramètre *nCmdShow* de [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Pour les processus de console, utilisez la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) pour spécifier les propriétés de la fenêtre uniquement lors de la création d’une console (à l’aide de [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) avec Create \_ New \_ console ou avec la fonction [**AllocConsole**](/windows/console/allocconsole) ). La structure **STARTUPINFO** peut être utilisée pour spécifier les propriétés suivantes de la fenêtre de console :

-   Taille de la nouvelle fenêtre de console, en cellules de caractères.
-   Emplacement de la nouvelle fenêtre de console, en coordonnées d’écran.
-   Taille, en cellules de caractères, de la mémoire tampon d’écran de la nouvelle console.
-   Attributs de couleur de texte et d’arrière-plan de la mémoire tampon d’écran de la nouvelle console.
-   Titre de la nouvelle fenêtre de la console.

 

 
