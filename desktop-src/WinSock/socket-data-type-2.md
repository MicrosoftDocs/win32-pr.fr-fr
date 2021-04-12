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
# <a name="socket-data-type"></a><span data-ttu-id="c1be5-103">Type de données Socket</span><span class="sxs-lookup"><span data-stu-id="c1be5-103">Socket Data Type</span></span>

<span data-ttu-id="c1be5-104">Dans les applications Winsock, un descripteur de socket n’est pas un descripteur de fichier et doit être utilisé avec les fonctions Winsock.</span><span class="sxs-lookup"><span data-stu-id="c1be5-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="c1be5-105">Dans UNIX, un descripteur de socket est représenté par un descripteur de fichier standard.</span><span class="sxs-lookup"><span data-stu-id="c1be5-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="c1be5-106">Par conséquent, un descripteur de socket sur UNIX peut être passé à l’une des fonctions d’e/s de fichier standard (par exemple, en lecture et en écriture).</span><span class="sxs-lookup"><span data-stu-id="c1be5-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="c1be5-107">En outre, tous les descripteurs dans UNIX, y compris les descripteurs de socket, sont de petits entiers non négatifs, et certaines applications font des suppositions que cela est vrai.</span><span class="sxs-lookup"><span data-stu-id="c1be5-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="c1be5-108">Les handles Windows Sockets n’ont pas de restrictions, à part que la valeur socket non valide \_ n’est pas un socket valide.</span><span class="sxs-lookup"><span data-stu-id="c1be5-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="c1be5-109">Les handles de socket peuvent prendre n’importe quelle valeur comprise entre 0 et socket non valide \_ – 1.</span><span class="sxs-lookup"><span data-stu-id="c1be5-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="c1be5-110">Étant donné que le type de **Socket** est non signé, la compilation du code source existant à partir de, par exemple, un environnement UNIX peut entraîner des avertissements du compilateur concernant des incompatibilités de type de données signé/non signé.</span><span class="sxs-lookup"><span data-stu-id="c1be5-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="c1be5-111">Cela signifie, par exemple, que la vérification des erreurs lors du retour des fonctions [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ne doit pas être effectuée en comparant la valeur de retour avec – 1, ou en vérifiant si la valeur est négative (approches courantes et légales dans UNIX).</span><span class="sxs-lookup"><span data-stu-id="c1be5-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="c1be5-112">Au lieu de cela, une application doit utiliser le socket de constante de manifeste non valide \_ tel que défini dans le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="c1be5-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="c1be5-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c1be5-113">For example:</span></span>

<span data-ttu-id="c1be5-114">Style BSD UNIX classique</span><span class="sxs-lookup"><span data-stu-id="c1be5-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="c1be5-115">Style préféré</span><span class="sxs-lookup"><span data-stu-id="c1be5-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="c1be5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1be5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1be5-117">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="c1be5-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c1be5-118">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="c1be5-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



