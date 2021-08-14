---
title: Points de connexion
description: Un objet point de connexion contient des données relatives à une ou plusieurs instances d’un service disponibles sur le réseau.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- points de connexion AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0b7a4c8ddbf592bba0ed39e2eb8f93faf863e6ebff7081865466b6522c98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022043"
---
# <a name="connection-points"></a>Points de connexion

Un objet point de connexion contient des données relatives à une ou plusieurs instances d’un service disponibles sur le réseau. La classe d’objet [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) est la classe de base abstraite à partir de laquelle les objets représentant des ressources connectables dans Active Directory Domain Services sont dérivés. L’illustration suivante montre certaines des classes d’objets dérivées de la classe d’objet **ConnectionPoint** .

![classes d’objets dérivées de la classe d’objet ConnectionPoint](images/connection-points.png)

Le tableau suivant répertorie les sous-classes immédiates de la classe [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) .



| Classe d’objet                                                    | Description                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Objets point de connexion de service (SCP) pour la publication de données que les applications clientes utilisent pour établir une liaison à un service. Pour plus d’informations, consultez [publication avec des points de connexion de service (SCP)](publishing-with-service-connection-points.md).                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Classe abstraite dont les sous-classes sont utilisées par le service de noms RPC (NS) accessible par le biais des fonctions **RpcNs \*** dans l’API Win32. Pour plus d’informations, consultez [publication avec le service de noms RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | objet de point de connexion utilisé par le service de nom d’inscription et de résolution de Windows sockets (RnR), accessible via les api **WSA \*** Windows sockets. pour plus d’informations, consultez [publication avec l’inscription et la résolution de Windows sockets (RnR)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**printQueue**](/windows/desktop/ADSchema/c-printqueue)                         | Objet point de connexion utilisé pour publier des imprimantes réseau. Pour plus d’informations, consultez [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**agrégat**](/windows/desktop/ADSchema/c-volume)                                 | Objet point de connexion utilisé pour publier les services de fichiers.                                                                                                                                                                                                                                                                   |



 

Sachez que les services basés sur COM n’utilisent pas d’objets de point de connexion pour se publier eux-mêmes. Ces services sont publiés dans le magasin de classes. le magasin de classes Windows 2000 est un référentiel basé sur répertoire pour toutes les applications COM, les interfaces et les api qui permettent la publication et l’attribution d’applications. Pour plus d’informations, consultez [publication de services com+](publishing-com-services.md).

 

 