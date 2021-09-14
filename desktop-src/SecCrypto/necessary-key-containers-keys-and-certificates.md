---
description: Les exemples de programmes dans les sections suivantes effectuent des opérations qui requièrent que les paires de clés publique/privée soient disponibles pour le chiffrement et le déchiffrement des fichiers, des messages et des signatures.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Conteneurs de clés, clés et certificats nécessaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123138"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Conteneurs de clés, clés et certificats nécessaires

Les exemples de programmes dans les sections suivantes effectuent des opérations qui requièrent que les [*paires de clés publique/privée*](../secgloss/p-gly.md) soient disponibles pour le chiffrement et le déchiffrement des fichiers, des messages et des signatures. La plupart de ces programmes se compilent, se lient et s’exécutent mais échouent au moment de l’exécution sans l’existence de [*conteneurs de clés*](../secgloss/k-gly.md), de clés, de [*magasins de certificats*](../secgloss/c-gly.md)et de certificats appropriés dans ces magasins.

En outre, certains des certificats du magasin MY doivent avoir certaines de leurs propriétés étendues définies.

La création du conteneur de clé par défaut nécessaire peut être effectuée en exécutant le programme dans l' [exemple de programme C : création d’un conteneur de clé et génération de clés](example-c-program-creating-a-key-container-and-generating-keys.md). Notez que la création d’un conteneur de clé ne génère pas automatiquement de paires de clés publiques/privées. L’exemple de programme, cependant, crée le conteneur de clé et génère les paires de clés publique/privée.

Une fois les paires de clés publiques/privées générées, vous pouvez obtenir des certificats de test à l’aide d’une [*autorité de certification*](../secgloss/c-gly.md) (ca).

Plusieurs programmes supposent que les certificats avec des noms d’objet spécifiques existent dans le magasin mon système. En particulier, plusieurs programmes recherchent les certificats dont le nom d’objet est « certificat de test complet » et « Hortense ». Les noms de sujet des certificats peuvent être modifiés dans le code pour correspondre aux noms de sujet des certificats qui existent dans le magasin de certificats MY.

L’exécution de l’exemple de programme dans l' [exemple de programme C : la liste des certificats dans un magasin](example-c-program-listing-the-certificates-in-a-store.md) affiche tous les certificats dans un magasin et toutes les propriétés étendues qui sont définies sur ces certificats.

 

 
