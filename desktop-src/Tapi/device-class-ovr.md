---
description: Les classes d’appareils simplifient le développement en permettant aux programmeurs de traiter des appareils qui ont des propriétés similaires de la même manière.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe d’appareil (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951967"
---
# <a name="device-class"></a>Classe d’appareil

Les classes d’appareils simplifient le développement en permettant aux programmeurs de traiter des appareils qui ont des propriétés similaires de la même manière. Par exemple, un téléphone numérique dans un bureau a généralement plus de fonctionnalités qu’un téléphone de base standard, mais les deux répondent pratiquement de la même façon à un ensemble de fonctions de base, et tous deux appartiennent à une classe d’appareil téléphonique. Les classes d’appareils permettent d’étendre l’interface TAPI en fournissant une infrastructure à partir de laquelle classifier et prendre en charge de nouveaux équipements.

Consultez [classes d’appareils TAPI](./tapi-device-classes.md) pour les classes définies par l’interface TAPI. Un fournisseur de services peut implémenter et définir des classes d’appareils supplémentaires pour l’équipement qu’il prend en charge. Une application n’a jamais besoin de savoir quel est le fournisseur de services qui contrôle l’appareil, mais peut nécessiter des informations sur le contrôle des nouvelles classes d’appareils.

Un fournisseur de services implémente une classe d’appareil en mappant les demandes dans les commandes d’appareil réelles. Par exemple, lorsque le fournisseur de services pour un modem compatible Hayes reçoit une commande transmise via TAPISVR pour effectuer un appel, il envoie des commandes AT classiques au modem.

L’interface du fournisseur de services peut être mappée à un large éventail d’environnements, y compris ceux qui ne sont généralement pas considérés comme appartenant à la téléphonie. Par exemple, la Conférence multimédia sur un réseau basé sur IP comme Internet.

Les développeurs d’applications doivent garder à l’esprit l’existence d’autres applications susceptibles de partager des services de téléphonie.

 

 
