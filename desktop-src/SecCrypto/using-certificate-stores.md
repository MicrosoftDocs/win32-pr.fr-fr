---
description: CAPICOM utilise des certificats numériques pour créer des signatures, chiffrer des clés de chiffrement de session lors de la création de messages enveloppés et déchiffrer les clés de session chiffrées lors de la réception d’un message enveloppé.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Utilisation des magasins de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417669"
---
# <a name="using-certificate-stores"></a>Utilisation des magasins de certificats

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

CAPICOM utilise des [*certificats numériques*](../secgloss/d-gly.md) pour créer des signatures, chiffrer des clés de chiffrement de session lors de la création de messages enveloppés et déchiffrer les clés de session chiffrées lors de la réception d’un message enveloppé. Par défaut, CAPICOM utilise des certificats du magasin My qui ont une clé privée associée pour la création de [*signatures numériques*](../secgloss/d-gly.md) et le déchiffrement de la clé de session. Dans la plupart des cas, une application n’a jamais besoin d’ouvrir ou de traiter directement un magasin de certificats.

Toutefois, les applications qui créent des messages enveloppés utilisent la [*clé publique*](../secgloss/p-gly.md) de chaque destinataire prévu d’un message enveloppé. Ces clés sont extraites des certificats des destinataires prévus. Ainsi, pour créer des messages enveloppés pour un groupe de destinataires prévus, les certificats de ces destinataires sont collectés dans un magasin de certificats.

Le tableau suivant répertorie les magasins de certificats standard qui sont normalement conservés sur une station d’utilisateur.



| Magasin        | Description                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Contient des certificats personnels. Ces certificats sont généralement associés à une clé privée.                                                                                                                                                                                                                                                                             |
| Les autres utilisateurs : | Contient les certificats de ceux à partir desquels l’utilisateur envoie normalement des messages enveloppés ou reçoit des messages signés.                                                                                                                                                                                                                                                     |
| Autorité de certification et racine  | Contient les [*certificats*](../secgloss/r-gly.md) des autorités de certification approuvées par l’utilisateur pour émettre des certificats pour d’autres utilisateurs. Les certificats de ces magasins sont normalement fournis avec le système d’exploitation ou par l’administrateur réseau de l’utilisateur. Les certificats dans le magasin racine sont généralement auto-signés. |



 

Des \_ magasins d’utilisateurs actuels CAPICOM supplémentaires \_ peuvent être créés, ouverts et rendus persistants en attribuant un nom de magasin différent sous forme de chaîne. Si un magasin portant ce nom n’existe pas, un magasin vide est créé et ouvert. Si un magasin existe, il est ouvert et tous les certificats qui se trouvent actuellement dans le magasin sont rendus disponibles.

Les sections suivantes présentent des exemples de tâches du magasin de certificats :

-   [Ouverture du magasin de Active Directory et récupération des certificats](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Ajout de certificats à un magasin de certificats](adding-certificates-to-a-certificate-store.md)
-   [Utilisation de magasins dans différents emplacements](using-stores-in-different-locations.md)
-   [Collecte et vérification des certificats](collecting-and-verifying-certificates.md)

 

 
