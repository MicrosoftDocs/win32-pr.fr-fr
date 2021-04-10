---
description: Répertorie et explique les étapes nécessaires à l’initialisation d’un package de sécurité.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Initialisation du package de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115066"
---
# <a name="initializing-the-security-package"></a>Initialisation du package de sécurité

Ces étapes sont nécessaires avant d’utiliser SSPI :

1.  La fonction d’initialisation doit être appelée pour obtenir l’adresse de la table de fonctions de sécurité.

    Le client et le serveur appellent [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) pour un pointeur vers une table de dispatch [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) . Ce tableau contient des pointeurs vers des fonctions de rappel déclarées dans SSPI. h. Ces pointeurs fournissent un accès aux implémentations de la DLL des différentes fonctions SSPI.

2.  Les informations doivent être obtenues sur les packages de sécurité pris en charge.

    Alors que la plupart des applications utilisent des packages de sécurité qui prennent en charge les fonctionnalités par défaut ou courantes, les packages de sécurité peuvent avoir des fonctionnalités uniques qui présentent un intérêt pour l’application. Une application nécessitant des fonctionnalités spéciales peut utiliser un package qui offre ces fonctionnalités. Pour plus d’informations, consultez [obtention d’informations sur les packages de sécurité](getting-information-about-security-packages.md).

À ce stade, l’application a initialisé avec succès un SSP et a choisi un package de sécurité avec des fonctionnalités suffisantes.

Le package [*Negotiate*](../secgloss/n-gly.md) peut être utilisé lorsque l’accord entre le client et le serveur sur le [*package de sécurité*](../secgloss/s-gly.md) à utiliser est effectué en arrière-plan. Si le package Negotiate n’est pas utilisé, le client et le serveur doivent s’accorder sur le package de sécurité spécifique à utiliser avant d’effectuer les étapes de configuration ci-dessus.

 

 
