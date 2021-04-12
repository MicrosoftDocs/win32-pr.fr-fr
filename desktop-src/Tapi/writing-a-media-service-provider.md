---
description: Un fournisseur de services multimédias doit implémenter un sous-ensemble minimal d’interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl et ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Écriture d’un fournisseur de services multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321442"
---
# <a name="writing-a-media-service-provider"></a>Écriture d’un fournisseur de services multimédia

Un fournisseur de services multimédias doit implémenter un sous-ensemble minimal d’interfaces MSPI : [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)et [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream). La prise en charge des sous-flux est facultative. En outre, un MSP donné peut implémenter des méthodes supplémentaires, telles que les contrôles requis pour le matériel spécialisé.

Les documents matériels suivants :

-   Les [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md), qui sont un ensemble de classes C++ conçues pour simplifier la tâche de création d’un MSP basé sur DirectShow. Les classes de base implémentent toutes les interfaces MSPI de manière générique. Les différents MSP peuvent remplacer les fonctions propres à MSP et fournir leurs propres implémentations.
-   Le [Gestionnaire de terminal TAPI 3](tapi-3-terminal-manager.md), qui fournit des interfaces et des méthodes utilisées par un MSP pour contrôler les terminaux.
-   [Terminaux enfichables](writing-a-pluggable-terminal.md), qui permettent à une application plutôt qu’à un MSP de créer des terminaux. Les développeurs qui ont déjà été expérimentés chez l’écriture de fournisseurs de services seront les créateurs principaux de terminaux enfichables. La version initiale mise en œuvre pour cette version est destinée aux applications de serveur de conférence qui doivent ajouter des clients non-Windows 2000 ou non multicast à des conférences de multidiffusion SDP/IP multifournisseurs TAPI 3.

 

 
