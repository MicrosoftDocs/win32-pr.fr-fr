---
title: Utilisation de mémoires tampons de chaîne
description: Les fonctions qui retournent des chaînes contiennent un paramètre d’entrée, Lpszbuffer a été et un paramètre de taille, lpdwBufferLength. Bien que Lpszbuffer a été puisse avoir la valeur NULL, lpdwBufferLength doit être un pointeur valide vers une variable DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518992"
---
# <a name="using-string-buffers"></a>Utilisation de mémoires tampons de chaîne

Les fonctions qui retournent des chaînes contiennent un paramètre d’entrée, *lpszbuffer a été* et un paramètre de taille, *lpdwBufferLength*. Bien que *lpszbuffer a été* puisse avoir la **valeur null**, *lpdwBufferLength* doit être un pointeur valide vers une variable **DWORD** . Si la mémoire tampon d’entrée vers laquelle pointe *lpszbuffer a été* a la **valeur null** ou est trop petite pour contenir la chaîne de sortie, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante**. La variable vers laquelle pointe *lpdwBufferLength* contient un nombre qui représente le nombre d’octets requis par la fonction pour retourner la chaîne demandée, y compris la marque de fin **null** . L’application doit allouer une mémoire tampon de cette taille, définir la variable vers laquelle pointe *lpdwBufferLength* et soumettre à nouveau la demande. Si la taille de la mémoire tampon est suffisante pour recevoir la chaîne demandée, la chaîne est copiée dans la mémoire tampon de sortie avec une marque de fin **null** et la fonction retourne un indicateur de réussite. La variable vers laquelle pointe *lpdwBufferLength* contient maintenant le nombre de caractères stockés dans la mémoire tampon, à l’exclusion de la marque de fin **null** .

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 