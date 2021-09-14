---
description: Le gestionnaire de transactions KTM (Kernel Transaction Manager) est un service de gestion des transactions. Il rend les transactions disponibles en tant qu’objets noyau et fournit des services de gestion des transactions aux composants système tels que le NTFS transactionnel (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: À propos de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094521"
---
# <a name="about-ktm"></a>À propos de KTM

Le gestionnaire de transactions KTM (Kernel Transaction Manager) est un service de gestion des transactions. Il rend les transactions disponibles en tant qu’objets noyau et fournit des services de gestion des transactions aux composants système tels que le [NTFS transactionnel](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

Les rubriques suivantes décrivent les utilisations et les fonctionnalités de KTM :

-   [Qu’est-ce qu’une transaction ?](what-is-a-transaction.md)
-   [Utilisation des transactions](programming-model.md)
-   [Écriture d’un Gestionnaire des ressources](writing-a-resource-manager.md)
-   [interopérabilité avec d’autres fonctionnalités de Windows](interoperability-with-other-windows-features.md)
-   [Sécurité KTM et droits d’accès](ktm-security-and-access-rights.md)

KTM s’appuie sur le [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) pour son fonctionnement. CLFS est un système de journalisation qui est capable d’activer des transactions.

 

 
