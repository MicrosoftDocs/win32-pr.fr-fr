---
description: Implémentez le NTFS transactionnel (TxF) et le registre transactionnel (TxR). TxF autorise les opérations de système de fichiers transactionnelles au sein de NTFS. TxR autorise les opérations de Registre transactionnelles. Coordonner les opérations du système de fichiers et du Registre avec une transaction.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gestionnaire de transactions du noyau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897529"
---
# <a name="kernel-transaction-manager"></a>Gestionnaire de transactions du noyau

## <a name="purpose"></a>Objectif

Le gestionnaire de transactions KTM (Kernel Transaction Manager) permet le développement d’applications qui utilisent des transactions. Le moteur de transactions se trouve dans le noyau, mais les transactions peuvent être développées pour les transactions en mode noyau ou utilisateur, et au sein d’un seul hôte ou de plusieurs hôtes distribués.

Le KTM est utilisé pour implémenter le NTFS transactionnel (TxF) et le registre transactionnel (TxR). TxF autorise les opérations de système de fichiers transactionnelles au sein du système de fichiers NTFS. TxR autorise les opérations de Registre transactionnelles. KTM permet aux applications clientes de coordonner les opérations du système de fichiers et du Registre avec une transaction.

Pour développer une application qui coordonne les transactions avec des ressources autres que TxF ou TxR, vous devez d’abord développer un service prenant en charge les transactions Win32, également appelé gestionnaire de ressources.

Les applications managées et COM+ doivent utiliser leurs gestionnaires de transactions natifs.

## <a name="where-applicable"></a>Le cas échéant

KTM peut être utilisé avec des applications et des gestionnaires de ressources hébergés sur Windows Vista ou Windows Server 2008.

## <a name="developer-audience"></a>Développeurs concernés

L’API KTM est conçue pour être utilisée par les programmeurs C et C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

le KTM est pris en charge à partir de Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                     | Description                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [À propos de](about-ktm.md)<br/>         | Informations générales sur les transactions et les fonctionnalités fournies par KTM.<br/>                           |
| [Référence](ktm-reference.md)<br/> | Documentation pour les fonctions, les structures de données, les énumérations et d’autres éléments de programmation KTM.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS transactionnel (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Coordinateur de transactions distribuées](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

