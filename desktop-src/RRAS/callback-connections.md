---
title: Connexions de rappel
description: RAS prend en charge les connexions dans lesquelles le serveur distant raccroche, puis rappelle le client pour établir la connexion.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007064"
---
# <a name="callback-connections"></a>Connexions de rappel

RAS prend en charge les connexions dans lesquelles le serveur distant raccroche, puis rappelle le client pour établir la connexion.

Pour chaque utilisateur qui peut se connecter à un serveur RAS, le serveur stocke un attribut de rappel qui contrôle la façon dont la connexion est établie. L’attribut par défaut n’est pas un rappel, ce qui signifie que l’utilisateur peut se connecter au serveur RAS sans un rappel. L’administrateur du serveur RAS peut également attribuer à un utilisateur l’attribut de rappel prédéfini ou défini par l’appelant.

Pour qu’un utilisateur ait affecté la restriction prédéfinie, l’administrateur spécifie un numéro de téléphone que le serveur RAS doit rappeler pour établir une connexion. L’utilisateur ne peut pas spécifier un autre numéro et la connexion ne peut pas être établie sans un rappel.

Une opération de rappel prédéfinie est gérée automatiquement par le gestionnaire de connexions d’accès à distance et le serveur distant. L’application cliente RAS n’a pas besoin d’effectuer d’autres opérations que de fournir des commentaires à l’utilisateur lorsque le gestionnaire de notification est appelé pendant les différents États de l’opération de rappel.

Un utilisateur affecté le privilège set by Caller peut choisir de se connecter avec ou sans rappel. L’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) utilise le membre **szCallbackNumber** de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) pour indiquer le choix.

Le membre **szCallbackNumber** peut simplement spécifier le numéro de rappel ; ou, pour établir la connexion sans rappel, **szCallbackNumber** peut pointer vers une chaîne vide, "". Dans l’un ou l’autre de ces cas, le gestionnaire de connexions d’accès à distance gère automatiquement l’opération de connexion. Comme pour une opération de rappel prédéfinie, le client RAS n’a pas besoin d’effectuer d’action autre que pour fournir des commentaires à l’utilisateur.

Si l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) active les [États suspendus](paused-states.md), **szCallbackNumber** peut pointer vers une chaîne d’astérisques, « \* », pour indiquer que l’opération de connexion doit passer à un état suspendu pour permettre à l’utilisateur de taper le numéro de rappel. Dans ce cas, l’opération de connexion pour un utilisateur défini par l’appelant passe à l’état suspendu après que le serveur distant a authentifié l’utilisateur. Au cours de l’état suspendu, le client RAS obtient l’entrée de numéro de rappel de l’utilisateur. Le client reprend ensuite l’opération de connexion en effectuant un deuxième appel de **rasdial** dans lequel **szCallbackNumber** spécifie le nombre fourni par l’utilisateur.

> [!Note]  
> Si les États suspendus ne sont pas activés, il existe une autre signification lorsque **szCallbackNumber** pointe vers une chaîne d’astérisques « \* ». Dans ce cas, l’astérisque indique que le numéro de rappel est stocké dans le fichier de l’annuaire téléphonique spécifié par l’appel [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

 

Dans le cas d’un rappel, l’appel à [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ne retourne pas de valeur tant que le serveur n’a pas rappelé le client.

 

 