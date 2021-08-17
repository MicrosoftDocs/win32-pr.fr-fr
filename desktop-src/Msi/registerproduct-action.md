---
description: L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes. en outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Action RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375960"
---
# <a name="registerproduct-action"></a>Action RegisterProduct

L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes. en outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.

L’action RegisterProduct configure les contrôles affichés par l’ajout/suppression de programmes dans le panneau de configuration. pour plus d’informations, consultez configuration de l' [ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action            |
|-------|---------------------------------------|
| \[1\] | Informations sur le produit inscrit. |



 

## <a name="remarks"></a>Remarques

L’action RegisterProduct n’est pas exécutée lors de l’installation sur un point d’installation d’administration.

 

 



