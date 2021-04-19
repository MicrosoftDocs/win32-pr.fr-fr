---
description: Le tableau suivant répertorie les interfaces COM TAPI version 3 par catégorie, par ordre d’importance.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Référence rapide des contrôles d’appel et de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106542089"
---
# <a name="call-and-media-controls-quick-reference"></a>Référence rapide des contrôles d’appel et de média

\[ Les [interfaces MSP ipconf](ipconf-msp-interfaces.md) ne sont pas utilisables dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le tableau suivant répertorie les interfaces COM TAPI version 3 par catégorie, par ordre d’importance. Les interfaces sont regroupées en fonction des cinq objets de contrôle d’appels de base de TAPI 3 : TAPI, Address, terminal, Call et CallHub. Les interfaces restantes sont regroupées en fonction des interfaces ACD (Automatic Call distribution), qui fournissent la fonctionnalité du centre d’appels. les interfaces d’énumérateur et les objets autonomes.



| Regroupements d’interfaces                                          | Description                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces d’objet TAPI](tapi-object-interfaces.md)         | L’objet TAPI est l’objet principal pour TAPI 3.                                                                                                                                                                                                              |
| [Interfaces d’objet Address](address-object-interfaces.md)   | L’objet Address représente une entité qui peut émettre ou recevoir des appels. Les interfaces et les méthodes associées permettent à une application d’extraire et de définir des informations relatives à l’adresse, par exemple si elle prend en charge l’ID de l’appelant.                             |
| [Interfaces d’objet terminal](terminal-object-interfaces.md) | L’objet terminal représente le récepteur ou la source au point de terminaison ou d’origine d’un appel. Les interfaces et les méthodes associées permettent à une application d’accéder et de définir des informations concernant le terminal, par exemple s’il est en cours d’utilisation. |
| [Appeler des interfaces d’objet](call-object-interfaces.md)         | L’objet d’appel représente un appel et est créé lorsqu’un appel arrive à exister. Les interfaces et les méthodes associées obtiennent et définissent des informations relatives à l’appel, telles que l’état d’appel actuel.                                                           |
| [Interfaces d’objet téléphonique](phone-object-interfaces.md)       | L’objet Phone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.                                                                                                                                                             |
| [Interfaces MSP IPConf](ipconf-msp-interfaces.md)           | Le MSP de conférence IP implémente plusieurs interfaces pour le contrôle de participant qui sont exposées sur l’objet d’appel.                                                                                                                                          |
| [Interfaces d’objet CallHub](callhub-object-interfaces.md)   | L’objet CallHub représente une vue tierce d’un appel à plusieurs parties. Les interfaces et les méthodes associées obtiennent et définissent des informations relatives à l’appel, par exemple si le concentrateur d’appels est actif.                                                          |
| [Interfaces d’énumérateur](enumerator-interfaces.md)           | Interfaces d’énumérateur COM-standard.                                                                                                                                                                                                                         |
| [Interfaces d’événements](./event-interfaces.md)            | Les interfaces d’événements sont également affichées avec leurs regroupements d’objets ou de fonctions.                                                                                                                                                                                |
| [Objets autonomes](stand-alone-objects.md)               | Les objets autonomes TAPI 3 fournissent des interfaces et des méthodes pour les opérations telles que la téléphonie assistée ou la gestion des événements.                                                                                                                    |



 

 

 
