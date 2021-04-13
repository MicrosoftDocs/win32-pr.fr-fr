---
title: Fonctions de sécurité
description: Les fonctions de sécurité de la gestion du réseau obtiennent et définissent des descripteurs de sécurité pour les racines de domaine et autonomes DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483848"
---
# <a name="security-functions"></a>Fonctions de sécurité

Les fonctions de sécurité de la gestion du réseau obtiennent et définissent des descripteurs de sécurité pour les racines de domaine et autonomes DFS.

Les fonctions de sécurité DFS sont répertoriées ci-dessous.

| Fonction                                                               | Description                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Obtient le descripteur de sécurité pour l’objet racine de la racine DFS spécifiée.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Localise l’objet racine pour la racine DFS spécifiée et définit le descripteur de sécurité fourni dessus.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Obtient le descripteur de sécurité pour l’objet conteneur de la racine autonome DFS spécifiée.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Localise l’objet conteneur pour la racine autonome DFS spécifiée et définit le descripteur de sécurité fourni dessus. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Obtient le descripteur de sécurité pour l’objet conteneur de la racine du domaine DFS spécifiée.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Localise l’objet conteneur pour la racine de domaine DFS spécifiée et définit le descripteur de sécurité fourni dessus.      |
