---
title: Comportement de réplication dans Active Directory Domain Services
description: Le comportement de réplication est cohérent et prévisible ; étant donné un ensemble de modifications apportées à un réplica donné, le résultat peut être prédit \ 8212 ; les modifications sont propagées à tous les autres réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, réplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7548ecf146f1d23b97b9db6a0307b21a6c39d359576c2de02285331d165fad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025137"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportement de réplication dans Active Directory Domain Services

Le comportement de réplication est cohérent et prévisible ; étant donné un ensemble de modifications apportées à un réplica donné, le résultat peut être prédit. les modifications seront propagées à tous les autres réplicas. La conception d’un modèle général fiable pour prédire quand les modifications seront appliquées à tous les autres réplicas, ou à un réplica particulier, est impossible, car l’état futur du système distribué dans son ensemble ne peut pas être connu. C’est ce que l’on appelle la « latence non déterministe » et les applications qui utilisent le répertoire doivent comprendre et autoriser ce dernier.

La situation n’est pas aussi complexe au moment où elle peut apparaître. Une application doit prendre en charge uniquement les trois États suivants :

-   Décalage de version : aucune des modifications appliquées à un réplica source donné n’a été propagée à un réplica de destination donné. Une application qui lit le réplica source voit la nouvelle version des informations, tandis qu’une application lisant la destination voit l’ancienne version (ou rien, si les nouvelles informations ont été ajoutées pour la première fois). La distorsion de version s’applique à tous les consommateurs de service d’annuaire.
-   Mise à jour partielle : certaines des modifications appliquées à un réplica source donné ont été propagées à un réplica de destination donné. Une application qui lit le réplica source voit les nouvelles informations, tandis qu’une application qui lit la destination voit une combinaison d’anciennes et de nouvelles informations (ou seulement certaines des nouvelles informations si les nouvelles informations ont été ajoutées pour la première fois). La mise à jour partielle s’applique aux consommateurs de service d’annuaire qui utilisent deux objets connexes ou plus pour stocker leurs informations.
-   État de la réplication complète : toutes les modifications appliquées à un réplica source donné ont été propagées à un réplica de destination donné. Les applications sur les réplicas de source et de destination voient les mêmes informations.

 

 




