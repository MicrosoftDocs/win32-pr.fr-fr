---
description: Les bitmaps dépendantes de l’appareil (DDB) sont décrites à l’aide d’une structure unique, la structure BITMAP.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Device-Dependent des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cf365b0f3b11e4a79bb0e7b1e1749d75ca356d41454e40cc6c31f383a74701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887235"
---
# <a name="device-dependent-bitmaps"></a>Device-Dependent des bitmaps

Les bitmaps dépendantes de l’appareil (DDB) sont décrites à l’aide d’une structure unique, la structure [**bitmap**](/windows/win32/api/wingdi/ns-wingdi-bitmap) . Les membres de cette structure spécifient la largeur et la hauteur d’une zone rectangulaire, en pixels ; largeur du tableau qui mappe les entrées de la palette d’appareils aux pixels ; et le format de couleur de l’appareil, en termes de plans de couleur et de bits par pixel. Une application peut récupérer le format de couleur d’un appareil en appelant la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) et en spécifiant les constantes appropriées. Notez qu’une DDB ne contient pas de valeurs de couleur ; au lieu de cela, les couleurs sont dans un format dépendant du périphérique. Pour plus d’informations, consultez [couleur dans les bitmaps](color-in-bitmaps.md). Étant donné que chaque périphérique peut avoir son propre ensemble de couleurs, une DDB créée pour un périphérique peut ne pas s’afficher correctement sur un autre appareil.

Pour utiliser une DDB dans un contexte de périphérique, elle doit avoir l’organisation de couleur de ce contexte de périphérique. Par conséquent, un DDB est souvent appelé *bitmap compatible* et il offre généralement de meilleures performances GDI qu’un dib. Par exemple, pour créer une image bitmap pour la mémoire vidéo, il est préférable d’utiliser une image bitmap compatible avec le même format de couleur que l’affichage principal. Une fois dans la mémoire vidéo, le rendu sur la bitmap et son affichage à l’écran sont beaucoup plus rapides qu’à partir d’une surface de mémoire système ou directement d’un DIB.

En plus d’activer de meilleures performances GDI, les bitmaps compatibles sont utilisées pour capturer des images (voir [capture d’une image](capturing-an-image.md) ) et pour créer des bitmaps au moment de l’exécution pour les menus, consultez « Création de l’image bitmap » dans (voir [utilisation de menus](../menurc/using-menus.md) ).

Pour transférer une image bitmap entre des appareils avec une organisation de couleurs différente, utilisez [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) pour convertir l’image bitmap compatible en dib et appelez [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) ou [**STRETCHDIBITS**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) pour afficher le fichier DIB sur le deuxième appareil.

Il existe deux types de DDB : Ignorable et ne peut pas être ignoré. Une DDB pouvant être ignorée est une bitmap que le système ignore si l’image bitmap n’est pas sélectionnée dans un contrôleur de réseau et si la mémoire système est insuffisante. La fonction [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) crée des bitmaps supprimables. Les fonctions [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)et [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) créent des bitmaps qui ne sont pas ignorables.

Une application peut créer un DDB à partir d’un DIB en initialisant les structures requises et en appelant la fonction [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) . La spécification de l' \_ initialisation CBM dans l’appel à **CreateDIBitmap** équivaut à appeler la fonction [**CREATECOMPATIBLEBITMAP**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) pour créer un DDB au format de l’appareil, puis à appeler la fonction [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) pour convertir les bits DIB en DDB. Pour déterminer si un appareil prend en charge la fonction **SetDIBits** , appelez la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant RC \_ di \_ bitmap comme indicateur RasterCaps.

 

 
