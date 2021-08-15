---
description: Le SCM prend en charge les types de handle pour autoriser l’accès aux objets suivants.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handles SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889187"
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

 

 



