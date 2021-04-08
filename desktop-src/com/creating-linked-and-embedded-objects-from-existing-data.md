---
title: Création d’objets liés et incorporés à partir de données existantes
description: Création d’objets liés et incorporés à partir de données existantes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675710"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>Création d’objets liés et incorporés à partir de données existantes

Un utilisateur assemble généralement un document composé à l’aide du presse-papiers ou du glisser-déplacer pour copier un objet de données de son application serveur vers l’application conteneur de l’utilisateur. Avec les applications qui prennent en charge OLE, l’utilisateur peut lancer le transfert à partir du serveur ou du conteneur. Par exemple, le serveur peut copier des données dans le presse-papiers de l’application serveur, puis basculer vers l’application conteneur et choisir coller un objet spécial/incorporé ou une commande de menu équivalente pour créer un nouvel objet incorporé à partir des données sélectionnées. Ou, l’utilisateur peut faire glisser les données d’une application à l’autre. Le processus est similaire pour la création d’un objet lié.

> [!Note]  
> Une application qui fonctionne comme un serveur OLE et un conteneur peut utiliser une sélection de ses propres données pour créer un objet incorporé ou lié à un nouvel emplacement dans le même document.

 

Le transfert de données entre le serveur OLE et les applications de conteneur repose sur le transfert de données uniforme, comme décrit dans [transfert de données](data-transfer.md). Les serveurs OLE et les gestionnaires d’objets implémentent [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) afin que leurs données soient disponibles pour les transferts à l’aide du presse-papiers ou du glisser-déplacer. Les objets OLE prennent en charge tous les formats de presse-papiers habituels. En outre, ils prennent en charge six formats de presse-papiers qui prennent en charge la création d’objets liés et incorporés à partir d’un objet de données sélectionné.

Les formats de presse-papiers OLE décrivent les objets de données qui, en cas de suppression ou de collage dans des conteneurs OLE, doivent devenir des objets incorporés ou liés à des documents composés. L’objet de données présente ces formats aux applications conteneur par ordre de fidélité comme description des données. En d’autres termes, l’objet présente le format le mieux représenté, suivi du meilleur format, et ainsi de suite. Ce classement intentionnel encourage une application de conteneur à utiliser le meilleur format possible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> <dt>

[Transfert de données](data-transfer.md)
</dt> </dl>

 

 




