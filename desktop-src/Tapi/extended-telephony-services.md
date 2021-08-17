---
description: L’API contient un mécanisme qui permet aux fournisseurs de fournisseurs de services d’étendre l’API de téléphonie à l’aide d’extensions spécifiques à l’appareil.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Services de téléphonie étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403f57904138b3797069222875086b0a4990b8e625f701f380120d65c235784e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140702"
---
# <a name="extended-telephony-services"></a>Services de téléphonie étendus

L’API contient un mécanisme qui permet aux fournisseurs de fournisseurs de services d’étendre l’API de téléphonie à l’aide d’extensions spécifiques à l’appareil. Les services de téléphonie étendus (ou services spécifiques au périphérique) incluent toutes les extensions de l’API définie par un fournisseur de services particulier. Étant donné que l’API définit uniquement le mécanisme d’extension, le fournisseur de services doit spécifier entièrement la définition du comportement de service Extended-Telephony.

## <a name="tapi-2x-extended-telephony"></a>Téléphonie étendue TAPI 2. x

Le mécanisme d’extension permet aux fournisseurs de fournisseurs de services de définir de nouvelles valeurs pour certains types énumération et indicateurs binaires, et d’ajouter des membres à la plupart des structures de données. L’interprétation des extensions est dérivée de l’identificateur d’extension du fournisseur de services, un identificateur pour la spécification de l’ensemble d’extensions pris en charge, qui peut traverser plusieurs fabricants. Des fonctions et des messages spéciaux, tels que [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) et [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) , sont fournis dans l’API pour permettre à une application de communiquer directement avec un fournisseur de services. Le fournisseur de services définit également les paramètres pour chaque fonction.

Les fournisseurs ne sont pas tenus de s’inscrire pour recevoir des identificateurs d’extension. Au lieu de cela, un utilitaire appelé EXTIDGEN (Extidgen.exe) est fourni dans le kit de développement logiciel (SDK) de la plateforme, qui autorise la génération locale d’identificateurs d’extension. Cet identificateur unique est composé d’une adresse de carte Ethernet, d’un nombre aléatoire et de l’heure de la journée. Un identificateur est assigné à un ensemble d’extensions (avant la distribution), et non à chaque instance individuelle d’une implémentation de ces extensions.

 

 
