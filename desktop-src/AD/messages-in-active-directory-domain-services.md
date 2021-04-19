---
title: Messages dans Active Directory Domain Services
description: Les messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6A (SP6a) et versions ultérieures avec DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Messages d’Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510188"
---
# <a name="messages-in-active-directory-domain-services"></a>Messages dans Active Directory Domain Services

Les messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6A (SP6a) et versions ultérieures avec DSClient. Ils sont également fonctionnels dans les stations de travail Windows 98/95 avec IE 4.01 et versions ultérieures et DSClient. Toutefois, si les pages de propriétés multisélections sont lancées à partir de l’interpréteur de commandes, le message d' [**erreur de \_ \_ notification \_ WM ADSPROP**](wm-adsprop-notify-error.md) et les fonctions d’assistance correspondantes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) et [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) ne sont pas fonctionnels et ne s’affichent pas. Si les pages de propriétés multisélections sont lancées au sein d’un outil d’administration, par exemple, utilisateurs et ordinateurs Active Directory, tous les messages sont fonctionnels et disponibles pour être affichés dans les pages de propriétés multisélections.

Active Directory Domain Services utiliser les messages suivants :

-   [**\_demande de \_ notification WM ADSPROP \_**](wm-adsprop-notify-apply.md)
-   [**notification de modification de la \_ notification WM ADSPROP \_ \_**](wm-adsprop-notify-change.md)
-   [**\_erreur de \_ notification WM ADSPROP \_**](wm-adsprop-notify-error.md)
-   [**notification de la sortie de \_ ADSPROP WM \_ \_**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ Notify \_ premier plan**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ Notify \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ Notify \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ Notify \_ SetFocus**](wm-adsprop-notify-setfocus.md)
-   [**création de la \_ feuille ADSPROP WM \_ \_**](wm-adsprop-sheet-create.md)
-   [**notification de fermeture de la \_ feuille du DSA WM \_ \_ \_**](wm-dsa-sheet-close-notify.md)
-   [**créer une notification de la \_ feuille DSA DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md)

 

 




