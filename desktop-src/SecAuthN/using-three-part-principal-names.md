---
description: Lorsque vous créez un package de sécurité SSP (Security Support Provider), vous ne devez pas autoriser le client joint à un domaine à s’authentifier auprès d’un contrôleur de domaine à l’aide d’un nom de fournisseur de services (SPN) en deux parties sous la forme suivante.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Utilisation de trois noms principaux de parties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ddc9ce552e71d97c5e795b7405e97803991133a96e7b3fac3e1a81bc45d5ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915181"
---
# <a name="using-three-part-principal-names"></a>Utilisation de trois noms principaux de parties

Lorsque vous créez un package de sécurité SSP (Security Support Provider), vous ne devez pas autoriser le client joint à un domaine à s’authentifier auprès d’un contrôleur de domaine à l’aide d’un nom de fournisseur de services (SPN) en deux parties sous la forme suivante.

-   <*protocole* >/< *nom d’hôte*>

Un client doit toujours s’authentifier en spécifiant le domaine.

-   <*protocole* >/< *nom* >/< d’hôte *nom de domaine*>

Un client joint à un domaine qui se connecte avec un SPN en deux parties peut être en mesure d’emprunter l’identité du contrôleur de domaine. Si vous autorisez deux noms de principal du service (SPN), vous devez créer une entrée de journal qui contient suffisamment d’informations pour permettre à l’administrateur d’identifier l’appelant.

 

 



