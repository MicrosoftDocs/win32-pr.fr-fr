---
description: Une application peut utiliser une police pour dessiner du texte uniquement si cette police réside sur un périphérique spécifié ou installée dans la table des polices système.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Installation et suppression de polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0184054973c769462ed8c1620e5534ff909576ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991233"
---
# <a name="font-installation-and-deletion"></a>Installation et suppression de polices

Une application peut utiliser une police pour dessiner du texte uniquement si cette police réside sur un périphérique spécifié ou installée dans la table des polices système. La table de polices est un tableau interne qui identifie toutes les polices non-périphériques disponibles pour une application. Une application peut récupérer les noms des polices actuellement installées sur un périphérique ou stockées dans la table de polices interne en appelant les fonctions [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) ou [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) .

Pour installer temporairement une police, appelez [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa). Ces fonctions chargent une police qui est stockée dans un fichier de ressources de police. Toutefois, il s’agit d’une installation temporaire, car après un redémarrage, la police n’est pas présente.

Pour installer une police qui restera après le redémarrage du système, utilisez l’une des méthodes suivantes :

-   Accédez au panneau de configuration, cliquez sur l’icône **polices** , puis sélectionnez **installer de nouvelles polices** dans le menu **fichier** . La police est disponible pour une application, même avant le redémarrage. Toutefois, dans une situation de serveur Terminal Server, la police est disponible pour la session active, mais elle n’est disponible pour les autres sessions qu’après un redémarrage.
-   Copiez la police dans le dossier% windir% \\ Fonts. Ensuite, accédez au panneau de configuration et cliquez sur l’icône **polices** , ou appelez [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa). La police est disponible pour une application, même avant le redémarrage. Toutefois, dans une situation de serveur Terminal Server, la police est disponible pour la session active, mais elle n’est disponible pour les autres sessions qu’après un redémarrage. Si vous copiez uniquement la police dans le dossier% windir% \\ Fonts, la police n’est disponible qu’après le redémarrage du système.

Quand une application se termine en utilisant une police installée, elle doit supprimer cette police en appelant la fonction [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) .

Une police installée à partir d’un emplacement autre que le dossier% windir% \\ Fonts ne peut pas être modifiée lorsqu’elle est chargée dans une session active, y compris la session 0. Toute tentative de modification, de remplacement ou de suppression sera donc bloquée. Si la modification d’une police est nécessaire :

-   Les *polices temporaires* sont chargées uniquement dans la session active. Avant de tenter toute modification de police, appelez [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) pour forcer la session active à décharger la police.
-   Les *polices permanentes* restent installées après le redémarrage et sont chargées par toutes les sessions créées. Appelez [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) pour forcer la session en cours à décharger la police. Ensuite, dans la clé de Registre font (**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ polices**), recherchez et supprimez la valeur de registre associée à la police. Enfin, redémarrez l’ordinateur pour vous assurer que la police n’est pas chargée dans une session. Après le redémarrage, effectuez la modification ou la suppression de la police.

Chaque fois qu’une application appelle les fonctions qui ajoutent et suppriment des ressources de police, elle doit également appeler la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) et envoyer un message [**WM \_ FONTCHANGE**](wm-fontchange.md) à toutes les fenêtres de niveau supérieur du système. Ce message avertit d’autres applications que la table de polices interne a été modifiée par une application qui a ajouté ou supprimé une police.

 

 
