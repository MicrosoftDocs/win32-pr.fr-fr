---
description: Cette rubrique décrit les types de classes de fenêtres, comment le système les localise et les éléments qui définissent le comportement par défaut des fenêtres qui leur appartiennent.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Classes de fenêtres (Windows et Messages)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b570309ce6613f3adfe256faff9c30b66f9dbd5062de5f342b434be32dce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849504"
---
# <a name="window-classes-windows-and-messages"></a>Classes de fenêtres (Windows et Messages)

Cette rubrique décrit les types de classes de fenêtres, comment le système les localise et les éléments qui définissent le comportement par défaut des fenêtres qui leur appartiennent.

Une classe de fenêtre est un ensemble d’attributs que le système utilise comme modèle pour créer une fenêtre. Chaque fenêtre est membre d’une classe de fenêtre. Toutes les classes de fenêtre sont spécifiques au processus.

### <a name="in-this-section"></a>Dans cette section



| Nom                                                 | Description                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des classes de fenêtre](about-window-classes.md)     | Présente les classes de fenêtre. Chaque classe de fenêtre a une procédure de fenêtre associée partagée par toutes les fenêtres de la même classe. La procédure de fenêtre traite les messages de toutes les fenêtres de cette classe et contrôle leur comportement et leur apparence.<br/> |
| [Utilisation des classes de fenêtre](using-window-classes.md)     | Montre comment inscrire une fenêtre locale et l’utiliser pour créer une fenêtre principale.<br/>                                                                                                                                                                     |
| [Référence de classe de fenêtre](window-class-reference.md) | Contient la référence de l’API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Fonctions de classe de fenêtre



| Nom                                         | Description                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Récupère des informations sur une classe de fenêtre, y compris un handle vers la petite icône associée à la classe de fenêtre. La fonction [**GetClassinfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) ne récupère pas de handle vers la petite icône.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Récupère la valeur 32 bits (**long**) spécifiée à partir de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associée à la fenêtre spécifiée. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Récupère la valeur spécifiée de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associée à la fenêtre spécifiée.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Récupère le nom de la classe à laquelle appartient la fenêtre spécifiée. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Récupère des informations sur la fenêtre spécifiée. La fonction récupère également la valeur 32 bits (**long**) à l’offset spécifié dans la mémoire de fenêtre supplémentaire.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Récupère des informations sur la fenêtre spécifiée. La fonction récupère également la valeur à un décalage spécifié dans la mémoire de fenêtre supplémentaire.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Inscrit une classe de fenêtre pour une utilisation ultérieure dans les appels à la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Inscrit une classe de fenêtre pour une utilisation ultérieure dans les appels à la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Remplace la valeur spécifiée au niveau de l’offset spécifié dans la mémoire de classe supplémentaire ou la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) pour la classe à laquelle appartient la fenêtre spécifiée.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Remplace la valeur de 16 bits (**Word**) à l’offset spécifié dans la mémoire de classe supplémentaire pour la classe de fenêtre à laquelle appartient la fenêtre spécifiée.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Modifie un attribut de la fenêtre spécifiée. La fonction définit également la valeur 32 bits (long) à l’offset spécifié dans la mémoire de fenêtre supplémentaire.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Modifie un attribut de la fenêtre spécifiée. La fonction définit également une valeur à l’offset spécifié dans la mémoire de fenêtre supplémentaire.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Annule l’inscription d’une classe de fenêtre, libérant ainsi la mémoire requise pour la classe. <br/>                                                                                                                                            |



 

Les fonctions suivantes sont obsolètes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></td>
<td>Récupère des informations sur une classe de fenêtre. <br/>
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassinfo</strong></a> a été remplacée par la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a> . Toutefois, vous pouvez toujours utiliser <strong>GetClassinfo</strong>, si vous n’avez pas besoin d’informations sur la petite icône de classe.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></td>
<td>Récupère la valeur de 16 bits (<strong>Word</strong>) à l’offset spécifié dans la mémoire de classe supplémentaire pour la classe de fenêtre à laquelle appartient la fenêtre spécifiée.
<blockquote>
[!Note]<br />
Cette fonction est déconseillée pour toute autre utilisation que <em>nIndex</em> définie sur GCW_ATOM. La fonction est fournie uniquement pour la compatibilité avec les versions 16 bits de Windows. Les applications doivent utiliser la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>Remplace la valeur 32 bits (<strong>longue</strong>) spécifiée à l’offset spécifié dans la mémoire de classe supplémentaire ou la structure <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> pour la classe à laquelle appartient la fenêtre spécifiée.
<blockquote>
[!Note]<br />
Cette fonction a été remplacée par la fonction <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> . pour écrire du code compatible avec les versions 32 bits et 64 bits de Windows, utilisez <strong>SetClassLongPtr</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>Structures de classe de fenêtre



| Nom                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contient les attributs de classe de fenêtre qui sont inscrits par la fonction [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . <br/> Cette structure a été remplacée par la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) utilisée avec la fonction [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Vous pouvez toujours utiliser [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) et [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) si vous n’avez pas besoin de définir la petite icône associée à la classe de fenêtre.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contient les informations de classe de fenêtre. Elle est utilisée avec les fonctions [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) et [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  . <br/> La structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) est similaire à la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Il existe deux différences. **WNDCLASSEX** inclut le membre **cbSize** , qui spécifie la taille de la structure et le membre **hIconSm** , qui contient un handle vers une petite icône associée à la classe de fenêtre.<br/> |



 

 

 
