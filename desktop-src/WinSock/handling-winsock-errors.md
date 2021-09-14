---
description: Gestion des erreurs dans Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Gestion des erreurs Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008268"
---
# <a name="handling-winsock-errors"></a>Gestion des erreurs Winsock

la plupart des Windows fonctions sockets 2 ne retournent pas la cause spécifique d’une erreur quand la fonction retourne. Certaines fonctions Winsock retournent la valeur zéro en cas de réussite. Dans le cas contraire, l’erreur de SOCKET de valeur \_ (-1) est retournée et un numéro d’erreur spécifique peut être récupéré en appelant la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Pour les fonctions Winsock qui renvoient un descripteur, une valeur de retour de socket non valide \_ (0xFFFF) indique une erreur et un numéro d’erreur spécifique peut être récupéré en appelant **WSAGetLastError**. Pour les fonctions Winsock qui retournent un pointeur, une valeur de retour **null** indique une erreur et un numéro d’erreur spécifique peut être récupéré en appelant la fonction **WSAGetLastError** .

Un code d’erreur Winsock peut être converti en HRESULT pour une utilisation dans un appel de procédure distante (RPC) à l’aide \_ de HRESULT à partir de \_ Win32. Dans les versions antérieures du kit de développement logiciel (SDK) de la plateforme, HRESULT \_ de \_ Win32 était défini en tant que macro dans le fichier d’en-tête *winerror. h* . dans le kit de développement logiciel (SDK) de Microsoft Windows, HRESULT \_ de \_ WIN32 est défini en tant que fonction inline dans le fichier d’en-tête *Winerror. h* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Codes d’erreur des sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



