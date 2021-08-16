---
description: Dans certaines situations, les clés doivent être exportées à partir de l’environnement sécurisé du fournisseur de services de chiffrement (CSP) dans l’espace de données d’une application. Les clés qui ont été exportées sont stockées dans des structures BLOB de clé chiffrée.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Stockage et Exchange de clé de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3028efb449b59deb24a7097369d8894d0876907f3555c836e95e14d8c4bf5cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768756"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Stockage et Exchange de clé de chiffrement

Dans certaines situations, les clés doivent être exportées à partir de l’environnement sécurisé du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) dans l’espace de données d’une application. Les clés qui ont été exportées sont stockées dans des structures [*blob de clé*](../secgloss/k-gly.md) chiffrée.

Il existe deux situations spécifiques où il est nécessaire d’exporter des clés :

-   Pour enregistrer une [*clé de session*](../secgloss/s-gly.md) en vue d’une utilisation ultérieure par une application, si, par exemple, une application vient de chiffrer un fichier de base de données à déchiffrer ultérieurement. L’application est chargée de stocker la clé de chiffrement. Cela est nécessaire, car les fournisseurs de services de chiffrement ne préservent pas les [*clés symétriques*](../secgloss/s-gly.md) d’une session à l’autres.
-   Pour envoyer une clé à une autre personne. Cela serait plus facile si les fournisseurs de services de chiffrement respectifs pouvaient communiquer directement, mais ils ne le peuvent pas. Étant donné que les fournisseurs de services de chiffrement ne peuvent pas communiquer, la clé doit être exportée à partir d’un CSP, transmise à l’application de destination, puis importée dans le CSP de destination. Ce processus peut devenir plus compliqué si le chemin de communication n’est pas approuvé.

Dans les deux cas, une application doit stocker une clé de session en dehors du CSP pendant un certain temps. Pour plus d’informations, consultez [procédure de stockage d’une clé de session](procedure-for-storing-a-session-key.md).

 

 
