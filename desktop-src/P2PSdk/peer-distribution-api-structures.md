---
description: Le service de distribution d’homologue Microsoft prend en charge les structures suivantes.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Structures de l’API de distribution d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc985ff7a1e8dccdaf9c26cee8380daeccbf4b803f563510c3524a9d5c0c2c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776029"
---
# <a name="peer-distribution-api-structures"></a>Structures de l’API de distribution d’homologue

Le service de distribution d’homologue Microsoft prend en charge les structures suivantes.



| Structure                                                              | Description                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informations de \_ base du client PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Indique si de nombreux clients téléchargent simultanément le même contenu.                                                                                                                                                                                             |
| [**\_étiquette de contenu PEERDIST \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Contient une balise fournie par le client qui est une valeur d’entrée pour [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). La balise est associée au segment de contenu et est utilisée dans les API de gestion de contenu, comme [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**\_options de publication PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Contient les options de publication, y compris les informations de version de l’API et les indicateurs d’option possibles.                                                                                                                                                                                           |
| [**OPTIONS de récupération d’HOMOLOGUe \_ \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Contient la version des informations de contenu à récupérer.                                                                                                                                                                                                                                 |
| [**\_informations sur l’État PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Contient des informations sur l’état actuel et les fonctionnalités du service BranchCache sur l’ordinateur local.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API de distribution d’homologue](peer-distribution-api-reference.md)
</dt> </dl>

 

 



