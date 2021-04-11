---
description: Un espace de noms d’objet protège les objets nommés de tout accès non autorisé.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Espaces de noms d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3eed750bc91c128251cc66fd7f9ed167771150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865410"
---
# <a name="object-namespaces"></a>Espaces de noms d’objets

Un *espace de noms d’objet* protège les objets nommés de tout accès non autorisé. La création d’un espace de noms privé permet aux applications et aux services de créer un environnement plus sécurisé.

Un processus peut créer un espace de noms privé à l’aide de la fonction [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) . Cette fonction requiert que vous spécifiiez une *limite* qui définit la façon dont les objets de l’espace de noms doivent être isolés. L’appelant doit se trouver dans la limite spécifiée pour que l’opération de création aboutisse. Pour spécifier une limite, utilisez les fonctions [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) et [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) .

Le paramètre *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) sert de nom de l’espace de noms. Chaque espace de noms est identifié de manière unique par son nom et ses limites. Le système prend en charge plusieurs espaces de noms privés portant le même nom, à condition qu’ils spécifient des limites différentes.

Supposons qu’un processus demande la création d’un espace de noms, NS1, qui définit une limite contenant deux éléments : le SID d’administrateur et le numéro de session actuel. L’espace de noms est créé si le processus s’exécute sous le compte administrateur dans la session spécifiée. Un autre processus peut accéder à cet espace de noms à l’aide de la fonction [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) . Le nom et la limite spécifiés doivent correspondre si ce processus permet d’ouvrir l’espace de noms créé par le premier processus. Notez qu’un processus peut ouvrir un espace de noms existant, même s’il n’est pas dans la limite, à moins que le créateur n’ait restreint l’accès à l’espace de noms à l’aide du paramètre *lpPrivateNamespaceAttributes* .

Les objets créés dans cet espace de noms ont des noms au format *préfixe* \\ *nomobjet*. Le préfixe est le nom de l’espace de noms spécifié par le paramètre *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea). Par exemple, pour créer un objet d’événement nommé MyEvent dans l’espace de noms NS1, appelez la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) avec le paramètre *LPNAME* défini sur NS1 \\ MyEvent.

Le processus qui a créé l’espace de noms peut utiliser la fonction [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) pour fermer le descripteur de l’espace de noms. Le handle est également fermé lorsque le processus qui a créé l’espace de noms se termine. Une fois le descripteur d’espace de noms fermé, les appels suivants à [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) échouent, mais toutes les opérations sur les objets de l’espace de noms réussissent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Espaces de noms d’objets de noyau](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
