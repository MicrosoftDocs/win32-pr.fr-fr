---
title: Messages dans Active Directory Domain Services
description: les Messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6a (SP6a) et versions ultérieures avec DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Messages d’Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025917"
---
# <a name="messages-in-active-directory-domain-services"></a>Messages dans Active Directory Domain Services

les Messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6a (SP6a) et versions ultérieures avec DSClient. ils sont également fonctionnels dans Windows stations de travail 98/95 avec ie 4.01 et versions ultérieures et DSClient. Toutefois, si les pages de propriétés multisélections sont lancées à partir de l’interpréteur de commandes, le message d' [**erreur de \_ \_ notification \_ WM ADSPROP**](wm-adsprop-notify-error.md) et les fonctions d’assistance correspondantes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) et [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) ne sont pas fonctionnels et ne s’affichent pas. Si les pages de propriétés multisélections sont lancées au sein d’un outil d’administration, par exemple, utilisateurs et ordinateurs Active Directory, tous les messages sont fonctionnels et disponibles pour être affichés dans les pages de propriétés multisélections.

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

 

 




