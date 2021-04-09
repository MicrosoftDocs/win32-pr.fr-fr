---
title: Énumération des réplicas d’une partition d’annuaire d’applications
description: Cette rubrique montre comment énumérer les réplicas pour une partition de l’annuaire d’applications.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Énumération des réplicas d’une partition de l’annuaire d’applications Active Directory
- Partitions de l’annuaire d’applications Active Directory, énumération des réplicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940829"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Énumération des réplicas d’une partition d’annuaire d’applications

Lorsqu’un réplica d’une partition d’annuaire d’applications est ajouté, le nom unique de l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) pour le contrôleur de domaine qui contiendra le réplica est ajouté à l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) . L’objet **crossRef** utilisé représente la partition de l’annuaire d’applications.

**Pour énumérer les réplicas d’une partition d’annuaire d’applications**

1.  Recherchez dans le conteneur de partitions un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dont la valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) est égale au nom unique de la partition d’annuaire d’applications.
2.  Utilisez chaque valeur de l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) pour effectuer la liaison à l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) du serveur.
3.  Obtenez l’ADsPath pour le parent de chaque objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) . Il s’agit d’un objet qui représente le serveur de contrôleur de domaine. Utilisez l’ADsPath pour établir une liaison à l’objet serveur.
4.  Obtenez la valeur d’attribut [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) de l’objet serveur. Il s’agit d’une propriété à valeur unique qui contient le nom DNS du serveur.

En raison de la latence de réplication et des retards planifiés de l’exécution du KCC, il est possible que les réplicas actifs réels pour une partition d’annuaire d’applications ne correspondent pas à la liste des contrôleurs de domaine indiquée par l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Une façon plus précise, mais moins efficace de déterminer les réplicas actifs réels d’une partition d’annuaire d’applications consiste à rechercher tous les objets [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) de la forêt qui ont un attribut [**MSDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) qui contient le nom unique de la partition de l’annuaire d’applications. L’attribut **MSDS-hasMasterNCs** contient les noms uniques de toutes les partitions d’annuaires accessibles en écriture que le contrôleur de domaine héberge, y compris les partitions d’annuaire d’applications.

 

 