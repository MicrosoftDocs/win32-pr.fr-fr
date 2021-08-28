---
description: Winsock fournit une interface de fournisseur de services pour la création de services Winsock, communément appelée SPI Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: À propos de Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f321aabfd6345e3209414f96dedfaca4b9ab0acfa1629d49883a72ab8199cfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996939"
---
# <a name="about-the-winsock-spi"></a>À propos de Winsock SPI

Winsock fournit une interface de fournisseur de services pour la création de services Winsock, communément appelée SPI Winsock. Il existe deux types de fournisseurs de services : les fournisseurs de transport et les fournisseurs d’espaces de noms. Les exemples de fournisseurs de transport incluent des piles de protocole telles que TCP/IP ou IPX/SPX, tandis qu’un exemple de fournisseur d’espace de noms serait une interface avec le système d’attribution de noms de domaine (DNS) d’Internet. Des sections distinctes de la spécification de l’interface du fournisseur de services s’appliquent à chaque type de fournisseur de services.

Les fournisseurs de services de [transport](transport-service-providers-2.md) et d' [espace de noms](name-space-service-providers-2.md) doivent être inscrits auprès de l' \_32.dll Ws2 au moment où ils sont installés. Cette inscription ne doit être effectuée qu’une seule fois pour chaque fournisseur, car les informations nécessaires sont conservées dans un stockage persistant.

 

 



