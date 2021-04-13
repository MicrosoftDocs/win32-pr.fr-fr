---
description: Étant donné que les sockets ne sont pas représentés par l’entier de style UNIX, petit et non négatif, l’implémentation de la fonction Select a été modifiée dans Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macros Select, FD_SET et FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528629"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macros Select, FD \_ set et FD \_ xxx

Étant donné que les sockets ne sont pas représentés par l’entier de style UNIX, petit et non négatif, l’implémentation de la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) a été modifiée dans Windows Sockets. Chaque ensemble de sockets est toujours représenté par la structure **FD \_ Set** , mais au lieu d’être stocké en tant que masque de masque, l’ensemble est implémenté en tant que tableau de Sockets. Pour éviter d’éventuels problèmes, les applications doivent adhérer à l’utilisation des \_ macros FD xxx pour définir, initialiser, effacer et vérifier les structures du [**\_ jeu FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



