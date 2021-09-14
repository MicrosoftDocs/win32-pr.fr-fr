---
title: Captures instantanées du système
description: Les instantanés sont au cœur des fonctions d’aide de l’outil. Un instantané est une copie en lecture seule de l’état actuel d’une ou plusieurs des listes suivantes qui résident dans les processus, les threads, les modules et les segments de mémoire système.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856587"
---
# <a name="snapshots-of-the-system"></a>Captures instantanées du système

Les instantanés sont au cœur des fonctions d’aide de l’outil. Un instantané est une copie en lecture seule de l’état actuel d’une ou plusieurs des listes suivantes qui résident dans la mémoire système : processus, threads, modules et tas.

Les processus qui utilisent les fonctions de l’aide de l’outil accèdent à ces listes à partir de captures instantanées plutôt que directement depuis le système d’exploitation. Les listes dans la mémoire système changent lorsque les processus sont démarrés et terminés, les threads sont créés et détruits, les modules exécutables sont chargés et déchargés de la mémoire système, et les tas sont créés et détruits. L’utilisation des informations d’un instantané empêche les incohérences. Dans le cas contraire, les modifications apportées à une liste peuvent éventuellement entraîner un thread à traverser la liste ou provoquer une violation d’accès (une erreur GP). Par exemple, si une application parcourt la liste des threads pendant que d’autres threads sont créés ou arrêtés, les informations que l’application utilise pour traverser la liste des threads peuvent devenir obsolètes et provoquer une erreur pour l’application qui parcourt la liste.

Pour prendre un instantané de la mémoire système, utilisez la fonction [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) . Vous pouvez contrôler le contenu d’un instantané en spécifiant une ou plusieurs des valeurs suivantes lors de l’appel de cette fonction :

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Les valeurs de **TH32CS \_ SNAPHEAPLIST** et **TH32CS \_ SNAPMODULE** sont spécifiques au processus. Lorsque ces valeurs sont spécifiées, le segment de mémoire et les listes de modules du processus spécifié sont inclus dans l’instantané. Si vous spécifiez zéro comme identificateur de processus, le processus actuel est utilisé. La valeur **TH32CS \_ SNAPTHREAD** crée toujours un instantané à l’ensemble du système même si un identificateur de processus est passé à [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).

Pour énumérer l’état du segment de mémoire ou du module pour tous les processus, spécifiez la valeur **\_ SNAPALL TH32CS** et l’identificateur de processus du processus actuel. Ensuite, pour chaque processus supplémentaire de l’instantané, appelez à nouveau [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , en spécifiant son identificateur de processus et la valeur **TH32CS \_ SNAPHEAPLIST** ou **TH32CS \_ SNAPMODULE** .

Vous pouvez récupérer un code d’état d’erreur étendu pour [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Lorsque votre processus se termine à l’aide d’un instantané, détruisez-le à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si vous ne détruisez pas un instantané, le processus perd de la mémoire jusqu’à ce qu’il se termine, auquel cas le système récupère la mémoire.

> [!Note]  
> Le descripteur d’instantané agit comme un descripteur de fichier et est soumis aux mêmes règles concernant les processus et les threads dans lesquels il peut être utilisé. Pour spécifier que le handle peut être hérité, créez l’instantané à l’aide de la valeur **\_ inherit TH32CS** .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réalisation d’un instantané et affichage des processus](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 