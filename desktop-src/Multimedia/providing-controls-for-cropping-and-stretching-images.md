---
title: Fournir des contrôles pour rogner et étirer des images
description: Fournir des contrôles pour rogner et étirer des images
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- MCIWndGetSource macro)
- MCIWndPutSource macro)
- MCIWndGetDest macro)
- MCIWndPutDest macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119465"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Fournir des contrôles pour rogner et étirer des images

MCIWnd vous permet de rogner et d’étirer des images d’un clip vidéo. Pour comprendre ces fonctionnalités, vous devez comprendre les relations entre la *taille de trame*, le *rectangle source*, le *rectangle de destination* et la *zone de lecture*.

Un clip vidéo est constitué de plusieurs images, chacune contenant une image. La taille de cadre d’un clip vidéo correspond à la taille de l’image dans le frame actuel. En règle générale, un clip vidéo a une taille de trame, car toutes les images du clip ont la même taille.

Le rectangle source est une zone rectangulaire qui recouvre les images d’un clip vidéo. Le rectangle source définit la partie de chaque frame affichée lors de la lecture. Lorsqu’un clip vidéo est chargé avec MCIWnd, le rectangle source est initialisé avec les mêmes dimensions et la même position que le cadre initial du clip vidéo.

Le rectangle de destination est une zone rectangulaire qui définit une fenêtre de lecture virtuelle. Le rectangle de destination reçoit les données de l’image du rectangle source pour chaque image du clip vidéo. Lorsque les dimensions du rectangle source et de destination sont différentes, MCIWnd ajuste les données de l’image horizontalement et verticalement en fonction des besoins pour remplir le rectangle de destination. Lorsqu’un clip vidéo est chargé avec MCIWnd, le rectangle de destination est initialisé avec les mêmes dimensions et la même position que le cadre initial du clip vidéo.

La zone de lecture est la partie d’une fenêtre MCIWnd utilisée par une application pour afficher le clip vidéo. La zone de lecture est la zone cliente d’une fenêtre MCIWnd ou la partie de la zone client qui exclut la barre d’outils MCIWnd. Quand un clip vidéo est chargé avec MCIWnd, la zone de lecture est initialisée avec les mêmes dimensions et la même position que le cadre initial du clip vidéo.

Vous pouvez rogner un clip vidéo à l’aide des macros [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) et [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) pour modifier le rectangle source. Le rognage d’une image détermine uniquement quelle partie des images sont affichées pendant la lecture ; elle ne modifie pas le contenu du fichier en cours de lecture. Avant de rogner une image, vous pouvez récupérer la taille actuelle du rectangle source à l’aide de **MCIWndGetSource**. Une fois la nouvelle taille et l’emplacement du rectangle source calculés, vous pouvez définir les limites de rognage du rectangle source à l’aide de **MCIWndPutSource**.

Vous pouvez étirer un clip vidéo à l’aide des macros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) et [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) pour modifier le rectangle de destination. Lorsque vous étirez un clip vidéo, vous augmentez ou réduisez la taille de cadre d’un clip vidéo verticalement, horizontalement ou dans les deux sens. Avant d’étirer une image, vous pouvez récupérer la taille et l’emplacement actuels du rectangle de destination à l’aide de **MCIWndGetDest**. La macro **MCIWndPutDest** vous permet de redéfinir le rectangle de destination. L’étirement peut déformer l’image pendant la lecture, mais elle ne modifie pas le contenu du fichier en cours de lecture.

Si la taille du rectangle de destination devient supérieure à celle de la zone de lecture, vous pouvez spécifier la partie de la zone de lecture qui affichera le clip vidéo à l’aide de **MCIWndPutDest**.

> [!Note]  
> La macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) ne modifie pas la taille de la zone de lecture. Pour étirer la fenêtre MCIWnd en même temps que le rectangle de destination, vous devez connaître la taille actuelle de la fenêtre MCIWnd et émettre de nouvelles dimensions de fenêtre en fonction du rectangle de destination. Vous pouvez récupérer les dimensions de la fenêtre MCIWnd à l’aide de la fonction [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) et redimensionner la fenêtre MCIWnd à l’aide de la fonction [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) .

 

 

 