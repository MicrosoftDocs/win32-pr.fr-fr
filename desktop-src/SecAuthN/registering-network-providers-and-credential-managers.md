---
description: Une fois que vous avez créé votre fournisseur réseau ou le gestionnaire d’informations d’identification, vous devez l’inscrire auprès du système.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009125"
---
# <a name="registering-network-providers-and-credential-managers"></a>Inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification

Une fois que vous avez créé votre fournisseur réseau ou le gestionnaire d’informations d’identification, vous devez l’inscrire auprès du système. Cela est nécessaire pour que le MPR sache quels fournisseurs de réseau sont installés. Au démarrage de MPR, il vérifie le registre et charge tous les fournisseurs de réseau ou gestionnaires d’informations d’identification qu’il trouve.

Étant donné que les fournisseurs de réseau et les gestionnaires d’informations d’identification sont liés, ils sont inscrits dans les mêmes sous-clés du Registre. En fait, les dll de fournisseur réseau peuvent également être des gestionnaires d’informations d’identification.

Pour obtenir des informations détaillées sur les clés de registre que vous devez créer pour votre fournisseur réseau ou le gestionnaire d’informations d’identification, consultez [clés de registre d’authentification](authentication-registry-keys.md).

 

 



