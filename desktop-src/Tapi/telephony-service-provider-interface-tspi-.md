---
description: Un fournisseur de services de téléphonie (TSPI) gère les contrôles spécifiques aux appareils pour la programmation des communications.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interface du fournisseur de services de téléphonie (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681799"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interface du fournisseur de services de téléphonie (TSPI)

Un fournisseur de services de téléphonie (TSPI) gère les contrôles spécifiques aux appareils pour la programmation des communications. Un TSP doit se conformer au fournisseur de services de téléphonie (TSPI) afin de fonctionner en tant que fournisseur de services au sein de l’environnement de téléphonie Microsoft. TSPI définit les fonctions externes exposées par un fournisseur de services de téléphonie fourni avec l’équipement de communication.

Un auteur TSP doit être familiarisé avec les documents de la [vue d’ensemble de la téléphonie Microsoft](./microsoft-telephony-overview.md), qui couvre l’architecture générale de téléphonie et fournit une vue d’ensemble des éléments communs à plusieurs API de téléphonie. Par exemple, cette section contient une liste d’opérations de contrôle de session, telles que Park, avec les descriptions de chaque opération et passe aux éléments de programmation TAPI 2,2, TAPI 3 et TSPI associés.

Les vues d’ensemble suivantes décrivent le matériel spécifique aux besoins de l’auteur d’un TSP. Notez que les parties les plus difficiles de l’écriture d’un TSP sont des détails spécifiques aux appareils et au système d’exploitation, qui n’entrent pas dans le cadre de ce document.

La vue d’ensemble de TSPI est divisée dans les sections suivantes :

-   Les [Considérations générales relatives](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) à la programmation couvrent les exigences des dll, la gestion correcte des versions, les vérifications des erreurs effectuées par TAPI, un résumé de la façon dont les fonctions TSPI correspondent aux fonctions TAPI 2,2 (TAPI/C) et une discussion sur les niveaux de service, comme exprimé dans TSPI.
-   Le [cycle de vie d’un fournisseur de services de téléphonie](life-cycle-of-a-telephony-service-provider.md) contient une synthèse générale des phases opérationnelles d’un TSP.
-   L' [accès aux appareils](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) couvre les principes fondamentaux de la façon dont un TSP expose les informations et les contrôles de l’appareil à l’interface TAPI.
-   [L’accès aux sessions](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) couvre ce que TAPI attend d’un TSP pendant une session de communication.
-   [L’accès aux médias](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) fournit un ensemble limité de contrôles sur les flux de médias. Un contrôle plus précis est possible grâce à l’utilisation d’un fournisseur de services de média, et les auteurs de fournisseurs de services doivent utiliser cette API chaque fois que cela est possible. TSPI fournit des communications entre une paire TSP/MSP.
-   les [appareils Téléphone](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) couvrent les informations supplémentaires et les opérations exposées si un TSP gère le contrôle de l’ensemble de téléphones. Ces opérations sont facultatives.
-   [L’interface DLL de l’interface utilisateur du fournisseur de services de téléphonie couvre des](the-telephony-service-provider-ui-dll-interface.md) fonctions spéciales qui peuvent être implémentées pour permettre à un utilisateur de définir directement de nombreux aspects des fonctionnalités d’un TSP.

Pour plus d’informations sur les éléments de programmation TSPI, consultez la [référence TSPI](tspi-reference.md) .

 

 
