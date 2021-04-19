---
description: L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes. En outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Action RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540857"
---
# <a name="registerproduct-action"></a>Action RegisterProduct

L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes. En outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.

L’action RegisterProduct configure les contrôles affichés par l’ajout/suppression de programmes dans le panneau de configuration. Pour plus d’informations, consultez Configuration de l' [Ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action            |
|-------|---------------------------------------|
| \[1\] | Informations sur le produit inscrit. |



 

## <a name="remarks"></a>Notes

L’action RegisterProduct n’est pas exécutée lors de l’installation sur un point d’installation d’administration.

 

 



