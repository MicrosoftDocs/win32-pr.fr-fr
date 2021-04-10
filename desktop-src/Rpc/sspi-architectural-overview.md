---
title: Vue d’ensemble de l’architecture SSPI
description: SSPI est une interface logicielle.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031586"
---
# <a name="sspi-architectural-overview"></a>Vue d’ensemble de l’architecture SSPI

SSPI est une interface logicielle. Les bibliothèques de programmation distribuées telles que RPC peuvent l’utiliser pour les communications authentifiées. Un ou plusieurs modules logiciels fournissent les fonctionnalités d’authentification réelles. Chaque module, appelé fournisseur SSP (Security Support Provider), est implémenté en tant que bibliothèque de liens dynamiques (DLL). Un SSP fournit un ou plusieurs packages de sécurité.

De nombreux SSP et packages sont disponibles. Windows est fourni avec le package de sécurité NTLM et le package de sécurité du protocole Microsoft Kerberos. En outre, vous pouvez choisir d’installer le package de sécurité SSL (Secure Socket Layer) ou tout autre fournisseur de services partagés compatible SSPI.

L’utilisation de SSPI garantit que, quel que soit le fournisseur de services partagés que vous sélectionnez, votre application accède aux fonctionnalités d’authentification de manière uniforme. Cette fonctionnalité offre à votre application une plus grande indépendance par rapport à l’implémentation du réseau que celle qui était disponible dans le passé.

Les applications distribuées communiquent par l’intermédiaire de l’interface RPC. Le logiciel RPC accède à son tour aux fonctionnalités d’authentification d’un fournisseur de services partagés par le biais de l’interface SSPI.

Pour plus d’informations, consultez [SSPI](/windows/desktop/SecAuthN/sspi).

 

 