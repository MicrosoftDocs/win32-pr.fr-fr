---
description: Dans les applications Winsock, un descripteur de socket n’est pas un descripteur de fichier et doit être utilisé avec les fonctions Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Type de données Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319802"
---
# <a name="socket-data-type"></a>Type de données Socket

Dans les applications Winsock, un descripteur de socket n’est pas un descripteur de fichier et doit être utilisé avec les fonctions Winsock.

Dans UNIX, un descripteur de socket est représenté par un descripteur de fichier standard. Par conséquent, un descripteur de socket sur UNIX peut être passé à l’une des fonctions d’e/s de fichier standard (par exemple, en lecture et en écriture).

En outre, tous les descripteurs dans UNIX, y compris les descripteurs de socket, sont de petits entiers non négatifs, et certaines applications font des suppositions que cela est vrai.

Les handles Windows Sockets n’ont pas de restrictions, à part que la valeur socket non valide \_ n’est pas un socket valide. Les handles de socket peuvent prendre n’importe quelle valeur comprise entre 0 et socket non valide \_ – 1.

Étant donné que le type de **Socket** est non signé, la compilation du code source existant à partir de, par exemple, un environnement UNIX peut entraîner des avertissements du compilateur concernant des incompatibilités de type de données signé/non signé.

Cela signifie, par exemple, que la vérification des erreurs lors du retour des fonctions [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ne doit pas être effectuée en comparant la valeur de retour avec – 1, ou en vérifiant si la valeur est négative (approches courantes et légales dans UNIX). Au lieu de cela, une application doit utiliser le socket de constante de manifeste non valide \_ tel que défini dans le fichier d’en-tête *Winsock2. h* . Par exemple :

Style BSD UNIX classique


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Style préféré


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



