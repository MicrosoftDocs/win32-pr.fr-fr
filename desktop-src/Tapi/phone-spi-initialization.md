---
description: Dans le cadre de l’abstraction de l’appareil téléphonique définie par TSPI, l’interface TAPI et le fournisseur de services doivent tout d’abord subir l’initialisation de base.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Téléphone Initialisation SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88465e31857ee9ecc3a54f98f98bf6d1d3b50b837d845dbf36af08be0ec78a7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072889"
---
# <a name="phone-spi-initialization"></a>Téléphone Initialisation SPI

Dans le cadre de l’abstraction de l’appareil téléphonique définie par TSPI, l’interface TAPI et le fournisseur de services doivent tout d’abord subir l’initialisation de base. Cette initialisation de base est effectuée à la fois pour les moitiés de ligne et de téléphone de l’interface par le même ensemble d’étapes. La première de ces étapes est la négociation de version d’interface. Pour ce faire, TAPI appelle la fonction [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) . Cette fonction est généralement utilisée pour négocier pour le compte d’un périphérique de ligne individuel ; des appareils de ligne différents au sein du même fournisseur de services peuvent fonctionner selon différentes versions d’interface. L’interface TAPI transmet une valeur d’identificateur d’appareil réservée spéciale, [**initialiser la \_ négociation**](initialize-negotiation.md), pour indiquer qu’elle négocie une version d’interface globale pour les fonctions d’initialisation qui affectent l’ensemble du fournisseur de services, à la fois pour les lignes et les téléphones.

Le résultat de cette négociation est passé aux procédures suivantes jusqu’à ce qu’un appareil téléphonique soit ouvert. À ce moment-là, l’appareil téléphonique est validé dans une version d’interface particulière. Cette version de l’interface est implicite jusqu’à la fermeture du téléphone et n’a pas besoin d’être transmise aux fonctions suivantes qui fonctionnent sur un téléphone ouvert.

À la suite de la négociation de version d’interface globale, TAPI appelle la fonction [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) . Cette fonction initialise le fournisseur de services, en lui donnant également les paramètres requis pour l’opération suivante. Ces paramètres sont les suivants :

-   *dwPermanentProviderID*: spécifie l’identificateur permanent du fournisseur de services initialisé, unique au sein des fournisseurs de services sur ce système.
-   *dwLineDeviceIDBase*: spécifie l’identificateur d’appareil le plus bas pour les appareils en ligne pris en charge par ce fournisseur de services.
-   *dwPhoneDeviceIDBase*: spécifie l’identificateur d’appareil le plus bas pour les appareils téléphoniques pris en charge par ce fournisseur de services. Les appareils de la classe de l’appareil téléphonique téléphonique sont identifiés par des entiers à partir de zéro. Cette plage d’identificateurs est contiguë sur la plage complète des appareils téléphoniques. Étant donné qu’il peut y avoir plusieurs fournisseurs de services gérant des appareils téléphoniques dans un même système, chaque fournisseur de services obtient une partie contiguë de la plage totale. Ce paramètre indique au fournisseur de services la valeur la plus faible dans sa partie de la plage. Le fournisseur de services, plutôt que TAPI, est chargé de mapper cette plage de variables à ses propres identificateurs d’appareil internes. Cela permet au fournisseur du fournisseur de services de disposer d’une flexibilité suffisante pour utiliser les identificateurs d’appareil dans les extensions spécifiques à l’appareil, si besoin. Étant donné que le fournisseur de services sait quels identificateurs d’appareil apparaissent dans les paramètres et les structures de données définis par TAPI, il peut utiliser des identificateurs d’appareil cohérents dans les paramètres d’extension et les structures de données spécifiques à l’appareil.
-   *dwNumLines*: spécifie le nombre d’appareils de ligne que ce fournisseur de services prend en charge.
-   *dwNumPhones*: spécifie le nombre d’appareils téléphoniques pris en charge par ce fournisseur de services.
-   *lpfnCompletionProc*: spécifie la procédure que le fournisseur de services appelle pour signaler l’achèvement de toutes les procédures de fonctionnement asynchrones sur les appareils de ligne et de téléphone.

Après [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), les opérations normales, telles que l’ouverture de téléphones, peuvent être effectuées.

 

 
