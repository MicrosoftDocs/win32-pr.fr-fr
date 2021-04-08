---
title: Modifier la valeur par défaut de la redirection de périphérique
description: Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840177"
---
# <a name="modify-device-redirection-default"></a>Modifier la valeur par défaut de la redirection de périphérique

Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.

Sur Windows Server 2008 R2 et versions ultérieures, les serveurs de passerelle Bureau à distance tentent par défaut d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance. Toutefois, cette fonctionnalité n’est pas prise en charge par certains serveurs. Par exemple, cela n’est pas pris en charge pour les connexions aux sessions de la console Hyper-V et il peut être nécessaire de désactiver la valeur par défaut pour prendre en charge l’authentification fédérée. Dans ce cas, cette fonctionnalité peut être désactivée en créant la clé de Registre suivante pour autoriser les connexions à traverser.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server Gateway \\ preRDPDisableRegKey**

Lorsque cette clé existe, la passerelle Bureau à distance n’applique pas la redirection de l’appareil.

 

 




