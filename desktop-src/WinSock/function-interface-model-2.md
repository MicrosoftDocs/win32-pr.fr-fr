---
description: Le transport et l’espace de noms Windows Sockets&\# 8211 ; les fournisseurs de services sont des dll avec un point d’entrée de procédure d’exportation unique pour la fonction d’initialisation du fournisseur de services WSPStartup ou NSPStartup, respectivement.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modèle d’interface de fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544659"
---
# <a name="function-interface-model"></a>Modèle d’interface de fonction

Espace de noms et transport Windows Sockets : les fournisseurs de services sont des dll avec un point d’entrée de procédure d’exportation unique pour la fonction d’initialisation du fournisseur de services [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) ou [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectivement. Toutes les autres fonctions du fournisseur de services sont rendues accessibles au \_32.dll Ws2 par le biais de la table de dispatch du fournisseur de services. Les DLL du fournisseur de services sont chargées en mémoire par le \_32.dll Ws2 uniquement lorsque cela est nécessaire, et sont déchargées lorsque leurs services ne sont plus nécessaires.

Le SPI définit également plusieurs circonstances dans lesquelles un fournisseur de services de transport appelle dans le \_32.dll (appels) Ws2 pour obtenir les services de prise en charge des dll. La DLL du fournisseur de services de transport reçoit la \_ table de distribution adcall de Ws232.dll via le paramètre *UpcallTable* pour [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).

L’extension de nom de fichier des fournisseurs de services doit être changée de « DLL » en «». WSP "ou". NSP». Cette exigence n’est pas stricte. Un fournisseur de services fonctionnera toujours avec l' \_32.dll Ws2 avec n’importe quelle extension de nom de fichier.

Le SPI Winsock utilise la Convention d’affectation de noms de préfixe de fonction suivante :

| Préfixe | Signification                          | Description                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Fournisseur de services Windows Sockets | Points d’entrée du fournisseur de services de transport           |
| WPU    | Appel du fournisseur de sockets Windows  | Ws2 \_32.dll points d’entrée pour les fournisseurs de services    |
| WSC    | Configuration de Windows Sockets    | WS2 \_32.dll points d’entrée pour les applets d’installation |
| LECTEURS    | Fournisseur d’espace de noms               | Points d’entrée du fournisseur d’espaces de noms                   |



 

Comme décrit ci-dessus, ces points d’entrée ne sont pas exportés (à l’exception de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) et [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), mais ils sont accessibles via un échange de tables de dispatch.

 

 



