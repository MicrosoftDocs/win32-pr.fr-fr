---
description: Dans la téléphonie Microsoft, les fournisseurs de services de téléphonie s’exécutent dans un processus distinct des applications de téléphonie.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interface DLL de l’interface utilisateur du fournisseur de services de téléphonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544848"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>Interface DLL de l’interface utilisateur du fournisseur de services de téléphonie

Dans la téléphonie Microsoft, les fournisseurs de services de téléphonie s’exécutent dans un processus distinct des applications de téléphonie. Les fournisseurs de services communiquent avec TAPISRV via l’interface TSPI (Telephony Service Provider Interface) et s’exécutent dans son processus. interface d’applications vers TAPI, qui sont chargées dans le contexte de l’application.

Les composants de l’interface TAPI utilisent différents mécanismes de communication interprocessus pour acheminer les demandes de fonction et les messages entre les applications et les fournisseurs de services. Les applications et les fournisseurs de services peuvent s’exécuter non seulement dans des processus distincts, mais aussi sur des systèmes complètement distincts. Par conséquent, les fournisseurs de services ne peuvent pas afficher de boîtes de dialogue dans le processus, ni même sur l’ordinateur sur lequel ils s’exécutent. L’interface utilisateur doit être appelée à partir du contexte de l’application, sur l’ordinateur sur lequel l’application s’exécute.

Cette section définit le mécanisme par lequel les fonctions d’interface utilisateur du fournisseur de services sont chargées et appelées dans le contexte de l’application. Un mécanisme est également défini par les fournisseurs de services qui peuvent ouvrir spontanément des boîtes de dialogue dans le contexte de l’application lorsque celles-ci ne seraient normalement pas attendues par l’application. C’est le cas, par exemple, de la boîte de dialogue **parler/raccrocher** qui est affichée par un fournisseur de services de modem de données lorsque le modem est utilisé en tant que numéroteur pour les appels vocaux interactifs, et l’utilisateur doit être invité à prendre le téléphone et à informer le fournisseur de services quand il doit placer le OnHook du modem.

 

 



