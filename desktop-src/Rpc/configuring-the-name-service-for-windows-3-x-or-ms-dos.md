---
title: configuration du Service de noms pour Windows 3. x ou MS-DOS
description: appel de procédure distante (RPC) et configuration du service de noms pour Windows 3. x ou MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009162"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>configuration du Service de noms pour Windows 3. x ou MS-DOS

Lorsque vous exécutez Setup.exe pour installer la bibliothèque Runtime RPC 16 bits, vous êtes invité à sélectionner un fournisseur de services de noms :

-   Si vous choisissez **installer le fournisseur de services de noms par défaut**, le NSP par défaut, Microsoft Locator, est installé.
-   Si vous choisissez **installer le fournisseur de services de noms personnalisés**, renseignez la boîte de dialogue **définir l’adresse réseau** pour installer le service d’annuaire de cellules/service d’annuaires de cellules DCE en tant que NSP. Le service d’annuaire de cellules/service d’annuaires de cellules DCE est le NSP utilisé avec les serveurs DCE.

L’adresse réseau est le nom de l’ordinateur hôte qui exécute le démon NSI (NSID). Cet ordinateur joue le rôle de passerelle vers le service d’annuaire de cellules/service d’annuaires de cellules DCE, en passant les appels de fonction NSI entre les ordinateurs qui exécutent des systèmes d’exploitation Microsoft et des ordinateurs DCE. L’adresse réseau peut comporter 80 caractères ou moins, par exemple, 11.1.9.169 est une adresse valide.

 

 




