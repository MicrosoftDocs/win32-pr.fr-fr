---
title: Capture de Still-Image
description: Capture de Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Message WM_CAP_GRAB_FRAME_NOSTOP
- Message WM_CAP_GRAB_FRAME
- capGrabFrameNoStop macro)
- capGrabFrame macro)
- Message WM_CAP_EDIT_COPY
- capEditCopy macro)
- Message WM_CAP_FILE_SAVEDIB
- capFileSaveDIB macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229955"
---
# <a name="still-image-capture"></a>Capture de Still-Image

Si vous souhaitez capturer une image en tant qu’image fixe, vous pouvez utiliser le message de [**\_ \_ \_ trame**](wm-cap-grab-frame.md) de trame de manipulation de l’embout de la [**\_ \_ \_ plage \_ WM**](wm-cap-grab-frame-nostop.md) (ou la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) ou [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ) pour capturer l’image numérisée dans une mémoire tampon de frame interne. Vous pouvez geler l’affichage sur l’image capturée à l’aide du cadre de manipulation de l' \_ embout WM \_ \_ . Dans le cas contraire, utilisez WM \_ Cap- \_ \_ frame \_ nostop.

Une fois capturés, vous pouvez copier l’image pour une utilisation par d’autres applications. Vous pouvez copier une image à partir de la mémoire tampon de frame dans le presse-papiers à l’aide du message [**WM \_ Cap \_ Edit \_ Copy**](wm-cap-edit-copy.md) (ou de la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). Vous pouvez également copier l’image à partir de la mémoire tampon de frame vers une image bitmap indépendante du périphérique (DIB) à l’aide du message [**\_ \_ \_ SAVEDIB de fichier WM**](wm-cap-file-savedib.md) (ou de la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).

Votre application peut également utiliser les deux messages de capture d’image unique pour modifier un frame de séquence par cadre, ou pour créer une séquence de photographie temporelle.

 

 




