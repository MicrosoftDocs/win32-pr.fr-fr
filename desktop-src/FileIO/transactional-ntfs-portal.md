---
description: Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transactionnel (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431909"
---
# <a name="transactional-ntfs-txf"></a>NTFS transactionnel (TxF)

\[Microsoft recommande vivement aux développeurs d’utiliser d’autres moyens pour répondre aux besoins de votre application. De nombreux scénarios pour lesquels TxF a été développé peuvent être obtenus à l’aide de techniques plus simples et plus facilement disponibles. En outre, TxF ne sera peut-être pas disponible dans les versions futures de Microsoft Windows. Pour plus d’informations et pour obtenir des alternatives à TxF, consultez [alternatives à l’utilisation de NTFS transactionnel](deprecation-of-txf.md).\]

## <a name="purpose"></a>Fonction

Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction. Les transactions TxF augmentent la fiabilité des applications en protégeant l’intégrité des données des défaillances et simplifient le développement d’applications en réduisant considérablement la quantité de code de gestion des erreurs.

TxF utilise l’infrastructure de transaction fournie par le gestionnaire de transactions KTM ( [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) ). cela permet aux opérations de fichier TxF de faire partie d’une transaction impliquant d’autres sources de données telles que SQL Server et le registre transactionnel (TxR).

## <a name="where-applicable"></a>Le cas échéant

Une application peut utiliser TxF pour préserver l’intégrité des données sur le disque suite à des conditions d’erreur inattendues et aider à résoudre des scénarios d’utilisateur de système de fichiers simultanés en isolant les modifications apportées par d’autres utilisateurs pendant les modifications.

## <a name="developer-audience"></a>Développeurs concernés

Avant d’utiliser TxF, vous devez avoir une connaissance opérationnelle des transactions à l’aide de KTM ou [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).

## <a name="run-time-requirements"></a>Conditions d’exécution

TxF est disponible à partir de Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                    | Description                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [À propos de](about-transactional-ntfs.md)<br/>         | Informations générales sur le NTFS transactionnel.<br/>                                                   |
| [Référence](transactional-ntfs-reference.md)<br/> | Documentation pour les fonctions, les structures de données, les énumérations et d’autres éléments de programmation.<br/> |



 

 

