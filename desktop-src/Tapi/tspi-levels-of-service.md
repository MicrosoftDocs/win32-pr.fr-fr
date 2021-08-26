---
description: L’interface TAPI divise les services de communication en basique, supplémentaire et étendu. Pour plus d’informations, consultez niveaux de service TAPI.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: Niveaux de service TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c72f09f7a076364918815ba5fdb79591f6f5b12382ac2aa529e0859eec53f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012129"
---
# <a name="tspi-levels-of-service"></a>Niveaux de service TSPI

L’interface TAPI divise les services de communication en basique, supplémentaire et étendu. Pour plus d’informations, consultez [niveaux de service TAPI](./tapi-levels-of-service.md) .

Un TSP est requis pour implémenter toutes les fonctions de téléphonie de base. Les [fonctions de téléphonie de base TSPI](tspi-basic-telephony-functions.md) contiennent un résumé de ces fonctions.

La téléphonie supplémentaire comprend des fonctionnalités disponibles sur les PBX modernes, telles que le maintien, le transfert, la Conférence, le stationnement, etc. Un fournisseur de services doit fournir un service de téléphonie supplémentaire uniquement s’il peut implémenter la signification exacte telle qu’elle est définie par l’interface TAPI. Si ce n’est pas le cas, la fonctionnalité doit être fournie en tant que service de téléphonie étendu. Toutes les fonctionnalités supplémentaires sont facultatives. Un fournisseur de services spécifie les services qu’il prend en charge via les réponses à des fonctions telles que [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) ou [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Un seul service supplémentaire peut être constitué de plusieurs appels et messages de fonction. Téléphone services d’appareil font partie d’une téléphonie supplémentaire.

Les services de téléphonie étendus permettent à un fournisseur d’implémenter des fonctions spécifiques à l’appareil. Le fournisseur de services doit identifier les extensions de manière unique à l’aide d’un *identificateur d’extension*. Les applications récupèrent et utilisent cet identificateur unique pour déterminer les extensions prises en charge par le fournisseur de services.

Les extensions peuvent s’appliquer à plusieurs fabricants. Des fonctions et des messages spéciaux, tels que [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) et [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) , sont fournis dans TAPI. Elles sont utilisées pour permettre l’extension de l’ensemble de fonctions (contrairement aux énumérations, aux indicateurs de bits et aux membres de structure de données) prises en charge par le fournisseur de services. Les paramètres de chaque fonction sont également définis par le fournisseur de services.

Un identificateur est assigné à un ensemble d’extensions (avant la distribution), et non à chaque instance individuelle d’une implémentation de ces extensions. L’utilitaire EXTIDGEN dans TSPI génère des identificateurs d’extension uniques pour les fournisseurs de services. Il utilise une adresse Ethernet-Adapter, un nombre aléatoire et l’heure de la journée pour générer un identificateur. il est donc extrêmement improbable que l’identificateur d’extension résultant soit en conflit avec un autre fournisseur de services. Par conséquent, les fournisseurs n’ont pas besoin d’inscrire des identificateurs d’extension.

L’utilitaire EXTIDGEN ne génère pas d’identificateurs d’extension, sauf si l’ordinateur sur lequel il est exécuté exécute également NetBIOS ou un autre logiciel réseau.

 

 
