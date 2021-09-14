---
title: Autoriser l’utilisateur à spécifier des appareils et des fichiers
description: Autoriser l’utilisateur à spécifier des appareils et des fichiers
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog macro)
- MCIWndOpen macro)
- MCIWndOpenInterface macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007290"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Autoriser l’utilisateur à spécifier des appareils et des fichiers

Vous pouvez associer un appareil ou un fichier à une fenêtre MCIWnd existante à l’aide des macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)et [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) , ainsi que de la fonction [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .

Pour permettre à un utilisateur de votre application de sélectionner un fichier à lire, utilisez **MCIWndOpenDialog**. Cette macro affiche la boîte de dialogue **ouvrir** (illustrée dans la capture d’écran suivante) pour le choix d’un fichier et associe le fichier sélectionné à la fenêtre MCIWnd actuelle.

![image fenêtre MCIWnd](images/mciwnd3.gif)

Vous pouvez permettre à un utilisateur de votre application de sélectionner un fichier à associer à une fenêtre MCIWnd et d’afficher un aperçu de ce fichier à l’aide de [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) et [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen). La fonction **GetOpenFileNamePreview** affiche la boîte de dialogue **ouvrir** permettant de choisir un fichier et permet à l’utilisateur d’afficher un aperçu (lecture) de son contenu. Lorsque le nom d’un fichier existant est spécifié dans la boîte de dialogue, **GetOpenFileNamePreview** fournit un petit contrôle pour permettre à l’utilisateur d’afficher un aperçu du contenu du fichier. Vous pouvez associer un fichier spécifié, sélectionné avec **GetOpenFileNamePreview** ou spécifié d’une autre manière, avec une fenêtre MCIWnd à l’aide de **MCIWndOpen**.

Vous pouvez également utiliser **MCIWndOpen** pour spécifier un appareil à associer à une fenêtre MCIWnd. Par exemple, vous pouvez utiliser un nom de périphérique, tel que « CDAudio ».

Pour associer une fenêtre MCIWnd à une interface de fichier ou une interface de flux de données à des données multimédias, utilisez la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) . Pour plus d’informations sur les interfaces de fichiers et de flux de données, consultez [fonctions et macros avifile](avifile-functions-and-macros.md).

> [!Note]  
> Avant d’associer un nouveau fichier ou un nouveau périphérique à une fenêtre MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) et [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) Fermez tout appareil actuellement associé à la fenêtre. Votre application n’a pas besoin de fermer les appareils ouverts avant d’utiliser ces macros.

 

 

 




