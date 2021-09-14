---
description: Le SCM prend en charge les types de handle pour autoriser l’accès aux objets suivants.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handles SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416336"
---
# <a name="scm-handles"></a>Handles SCM

Le SCM prend en charge les types de handle pour autoriser l’accès aux objets suivants.

-   Base de données des services installés.
-   Service.
-   Verrou de base de données.

Un objet SCManager représente la base de données de services installés. Il s’agit d’un objet conteneur qui contient des objets de service. La fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) retourne un handle à un objet SCManager sur un ordinateur spécifié. Ce descripteur est utilisé lors de l’installation, de la suppression, de l’ouverture et de l’énumération des services et du verrouillage de la base de données de services.

Un objet de service représente un service installé. Les fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) retournent des handles aux services installés.

Les fonctions [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)et [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) peuvent demander différents types d’accès aux SCManager et aux objets de service. L’accès demandé est accordé ou refusé en fonction du jeton d’accès du processus appelant et du descripteur de sécurité associé à l’objet de service ou SCManager.

La fonction [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) ferme les handles des objets SCManager et service. Lorsque vous n’avez plus besoin de ces handles, veillez à les fermer.

 

 



