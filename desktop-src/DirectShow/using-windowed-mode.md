---
description: Utilisation du mode fenêtre
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Utilisation du mode fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534351"
---
# <a name="using-windowed-mode"></a>Utilisation du mode fenêtre

> [!Note]  
> Le [filtre de convertisseur vidéo](video-renderer-filter.md) hérité utilise toujours le mode fenêtre. Les filtres VMR-7 et VMR-9 utilisent le mode fenêtre par défaut, mais prennent également en charge le mode sans fenêtre.

 

En mode fenêtre, le convertisseur vidéo crée sa propre fenêtre dans laquelle il peint les images vidéo. À moins que vous ne spécifiiez sinon, cette fenêtre est une fenêtre de niveau supérieur avec ses propres bordures et barre de titre. La plupart du temps, toutefois, vous attachez la fenêtre vidéo à une fenêtre d’application, de sorte que la vidéo est intégrée à l’interface utilisateur de votre application. Ce processus implique les étapes suivantes :

1.  Requête pour **IVideoWindow**.
2.  Définissez la fenêtre parente.
3.  Définissez de nouveaux styles de fenêtre.
4.  Placez la fenêtre vidéo à l’intérieur de la fenêtre propriétaire.
5.  Notifier la fenêtre vidéo des \_ messages de déplacement WM.

**Requête pour IVideoWindow**

Avant de commencer la lecture, interrogez le gestionnaire du graphique de filtre pour l’interface **IVideoWindow** :


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Définir la fenêtre parente**

Pour définir la fenêtre parente, appelez la méthode [**IVideoWindow ::p ut \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) avec un handle vers la fenêtre de votre application. Cette méthode prend une variable de type [**OAHWND**](oahwnd.md), castant donc le handle en ce type :


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Définir de nouveaux styles de fenêtres**

Modifiez le style de la fenêtre vidéo en appelant la méthode [**IVideoWindow ::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



L' \_ indicateur WS Child définit la fenêtre comme une fenêtre enfant, et l’indicateur WS \_ CLIPSIBLINGS empêche la fenêtre de dessiner à l’intérieur de la zone cliente d’une autre fenêtre enfant.

**Positionner la fenêtre vidéo**

Pour définir la position de la vidéo par rapport à la zone cliente de la fenêtre d’application, appelez la méthode [**IVideoWindow :: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) . Cette méthode prend un rectangle qui spécifie le bord gauche, le bord supérieur, la largeur et la hauteur de la fenêtre vidéo. Par exemple, le code suivant étire la fenêtre vidéo pour l’adapter à la totalité de la zone cliente de la fenêtre parente :


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Pour connaître la taille native de la vidéo, appelez la méthode [**IBasicVideo :: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) sur le gestionnaire de graphique de filtre. Vous pouvez utiliser ces informations pour mettre à l’échelle la vidéo et conserver les proportions correctes.

**Répondre aux \_ messages WM Move**

Pour des performances optimales, vous devez notifier le convertisseur vidéo chaque fois que la fenêtre se déplace alors que le graphique est suspendu. Appelez la méthode [**IVideoWindow :: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) pour transférer le \_ message WM Move :


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Si le convertisseur utilise une superposition matérielle, cette notification entraîne la mise à jour de la position de superposition par le convertisseur. (Le VMR-9 n’utilise pas de superpositions, vous n’avez donc pas besoin d’appeler cette méthode si vous utilisez VMR-9).

**Nettoyer**

Avant de quitter l’application, arrêtez le graphique et redéfinissez le propriétaire de la fenêtre vidéo sur la **valeur null**. Sinon, les messages de fenêtre peuvent être envoyés à la mauvaise fenêtre, ce qui risque de provoquer des erreurs. Vous pouvez également masquer la fenêtre vidéo, ou une image vidéo scintillent momentanément à l’écran :


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Si le parent de la fenêtre vidéo est un enfant de votre fenêtre d’application principale (en d’autres termes, si la fenêtre vidéo est un enfant d’un enfant), vous devez créer la fenêtre vidéo à l’aide de **CoCreateInstance** et l’ajouter au graphique, au lieu de laisser le gestionnaire de graphes de filtre ajouter le convertisseur vidéo pendant la [connexion intelligente](intelligent-connect.md). Cela permet de s’assurer que la fenêtre vidéo et la fenêtre enfant sont repeintes en même temps. Dans le cas contraire, la fenêtre enfant peut être peinte sur la fenêtre vidéo.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 



