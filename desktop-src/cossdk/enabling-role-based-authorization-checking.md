---
description: Pour utiliser la sécurité basée sur les rôles dans votre application COM+, vous devez d’abord activer la vérification d’autorisation basée sur les rôles pour l’application.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Activation de la vérification d’autorisation Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095429"
---
# <a name="enabling-role-based-authorization-checking"></a>Activation de la vérification d’autorisation Role-Based

Pour utiliser la sécurité basée sur les rôles dans votre application COM+, vous devez d’abord activer la vérification d’autorisation basée sur les rôles pour l’application. Cela garantit que les utilisateurs qui accèdent à l’application sont vérifiés pour le rôle auquel ils appartiennent avant qu’ils soient autorisés à faire quoi que ce soit dans l’application. Si la vérification de l’autorisation basée sur les rôles n’est pas activée, la sécurité basée sur les rôles pour l’application n’est pas utilisée.

**Pour activer la vérification de l’autorisation basée sur les rôles**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous activez la vérification d’autorisation basée sur les rôles, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Sous **autorisation**, activez la case à cocher **appliquer les vérifications d’accès pour cette application** . Si vous désactivez la case à cocher, la sécurité basée sur les rôles n’est pas utilisée pour l’application.

4.  Cliquez sur **OK**.

Le paramètre d’autorisation sélectionné prend effet lors du prochain démarrage de l’application.

 

 



