---
title: Suppression d’une partition d’annuaire d’applications
description: Une partition d’annuaire d’applications est supprimée en supprimant l’objet crossRef qui représente la partition de l’annuaire d’applications.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Suppression d’une partition de l’annuaire d’applications Active Directory
- Partitions de l’annuaire d’applications Active Directory, suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724573"
---
# <a name="deleting-an-application-directory-partition"></a>Suppression d’une partition d’annuaire d’applications

Une partition d’annuaire d’applications est supprimée en supprimant l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition de l’annuaire d’applications. Lorsque la suppression de l’objet **crossRef** est répliquée sur un contrôleur de domaine qui a un réplica de la partition de l’annuaire d’applications, le KCC supprime le réplica local de la partition de l’annuaire d’applications. Cela finit par entraîner la suppression de tous les réplicas de la partition d’annuaire d’applications.

Lorsque l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) est supprimé, le serveur de Active Directory supprime l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) qui a été créé lors de la création de la partition d’annuaire d’applications, ainsi que la suppression de tous les objets de la partition de l’annuaire d’applications. Aucun des objets de la partition de l’annuaire d’applications n’est désactivé lorsqu’ils sont supprimés.

Lors de la suppression d’une partition d’annuaire d’applications, il est très difficile de la restaurer. Pour restaurer une partition d’annuaire d’applications, il est nécessaire de restaurer une sauvegarde qui a un réplica de la partition d’annuaire d’applications, de Rechercher l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition d’annuaire d’applications et de restaurer l’objet **crossRef** faisant autorité.

**Pour supprimer une partition d’annuaire d’applications et ses réplicas, procédez comme suit :**

1.  Recherchez dans le conteneur de partitions un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dont la valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) est égale au nom unique de la partition d’annuaire d’applications.
2.  Supprimez l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Pour plus d’informations, consultez [exemple de code pour la suppression d’une partition d’annuaire d’applications](example-code-for-deleting-an-application-directory-partition.md).

 

 