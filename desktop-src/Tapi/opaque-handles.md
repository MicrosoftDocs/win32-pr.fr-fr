---
description: Quelques types définis par TSPI sont des handles opaques.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Handles opaques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527099"
---
# <a name="opaque-handles"></a>Handles opaques

Quelques types définis par TSPI sont des handles opaques. Celles-ci sont utilisées dans TSPI comme références publiques à des structures de données privées. Cela permet de vérifier le type des paramètres fournis aux procédures d’interface tout en donnant une mesure de protection de type. Seul le propriétaire de la structure de données privées sait comment interpréter le type opaque comme une référence à sa représentation de structure de données. À titre d’exemple d’utilisation de handles opaques, envisagez un appareil téléphonique. TAPI et le fournisseur de services gèrent généralement les structures de données représentant leurs vues respectives de l’appareil.

Dans les structures de données de téléphone classiques gérées par TAPI et un fournisseur de services, chacun contient un handle opaque pour l’autre structure de données. Celles-ci ont été échangées lors d’une étape d’initialisation précoce. Lorsque TAPI appelle une fonction TSPI, il passe le handle opaque pour faire référence à l’appareil. Le fournisseur de services sait comment le résoudre en tant que référence (flèche) à sa structure de données. Un processus similaire se produit lorsque le fournisseur de services appelle une fonction de rappel dans TAPI.

 

 



