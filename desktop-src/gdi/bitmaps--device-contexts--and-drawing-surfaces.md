---
description: Un contexte de périphérique (DC) est une structure de données qui définit les objets graphiques, leurs attributs associés et les modes graphiques qui affectent la sortie sur un appareil. Pour créer un contrôleur de périphérique, appelez la fonction CreateDC ; pour récupérer un contrôleur de périphérique, appelez la fonction GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Images bitmap, contextes de périphérique et surfaces de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202054"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Images bitmap, contextes de périphérique et surfaces de dessin

Un *contexte de périphérique* (DC) est une structure de données qui définit les objets graphiques, leurs attributs associés et les modes graphiques qui affectent la sortie sur un appareil. Pour créer un contrôleur de périphérique, appelez la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ; pour récupérer un contrôleur de périphérique, appelez la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .

Avant de retourner un descripteur qui identifie ce contrôleur de réseau, le système sélectionne une surface de dessin dans le contrôleur de réseau. Si l’application a appelé la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) pour créer un contexte de périphérique pour un affichage VGA, les dimensions de cette surface de dessin sont de 640 x 480 pixels. Si l’application a appelé la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , les dimensions reflètent la taille de la zone cliente.

Avant qu’une application puisse commencer à dessiner, elle doit sélectionner une image bitmap avec la largeur et la hauteur appropriées dans le DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Quand une application transmet le descripteur au contrôleur de l’une des fonctions de dessin GDI (Graphics Device Interface), la sortie demandée apparaît sur la surface de dessin sélectionnée dans le contrôleur de l’appareil.

Pour plus d’informations, consultez [contextes de périphérique mémoire](memory-device-contexts.md).

 

 



