---
description: Windows le programme d’installation 5,0 s’exécutant sur Windows Server 2008 R2 ou Windows 7 peut énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Énumération des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598e80e270d0442b06fdb6db50cc5b58df529a1305936f2610211f192c8572be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947040"
---
# <a name="enumerating-components"></a>Énumération des composants

Windows le programme d’installation 5,0 s’exécutant sur Windows Server 2008 R2 ou Windows 7 peut énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant. un package créé pour Windows Installer 5,0 peut utiliser les fonctions [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)et [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) pour rechercher des composants et des produits dans les comptes d’utilisateur et les contextes d’installation. Les fonctions [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)et [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) retournent uniquement des informations sur les composants et les produits installés pour le compte d’utilisateur qui a appelé la fonction. Plusieurs appels à ces fonctions, au moins une fois pour chaque compte d’utilisateur, sont nécessaires pour collecter des informations sur l’ordinateur entier.

La fonction [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) énumère les composants installés. La fonction récupère un code de composant chaque fois qu’elle est appelée. L' [**objet Component**](components.md) reçoit des informations sur un composant installé par cette fonction.

La fonction [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) énumère les produits qui sont des clients d’un composant installé spécifié. L' [**objet client**](client.md) reçoit des informations sur un client par cette fonction.

La fonction [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) retourne le chemin d’accès complet à un composant installé. La fonction retourne la clé de Registre si le chemin d’accès de la clé du composant est une clé de registre. L' [**objet ComponentInfo**](componentinfo.md) reçoit des informations sur un composant installé par cette fonction.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette fonctionnalité est disponible à partir de Windows Installer 5,0 s’exécutant sur Windows 7 ou Windows Server 2008 R2.

 

 



