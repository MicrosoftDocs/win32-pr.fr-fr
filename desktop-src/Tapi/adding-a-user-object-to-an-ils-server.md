---
description: Le fragment de code suivant illustre la publication d’un objet utilisateur dans un serveur ILS. Après la publication d’un objet utilisateur, les tiers distants peuvent utiliser l’objet utilisateur pour effectuer des appels à l’utilisateur spécifié.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Ajout d’un objet utilisateur à un serveur ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750781"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Ajout d’un objet utilisateur à un serveur ILS

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le fragment de code suivant illustre la publication d’un objet utilisateur dans un serveur ILS. Après la publication d’un objet utilisateur, les tiers distants peuvent utiliser l’objet utilisateur pour effectuer des appels à l’utilisateur spécifié.

Ce fragment part du principe que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée.


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



