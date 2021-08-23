---
title: Modifier la valeur par défaut de la redirection de périphérique
description: Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138168"
---
# <a name="modify-device-redirection-default"></a>Modifier la valeur par défaut de la redirection de périphérique

Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.

sur Windows server 2008 R2 et versions ultérieures, Bureau à distance serveurs de passerelle essaient par défaut d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de Session Bureau à distance. Toutefois, cette fonctionnalité n’est pas prise en charge par certains serveurs. Par exemple, cela n’est pas pris en charge pour les connexions aux sessions de la console Hyper-V et il peut être nécessaire de désactiver la valeur par défaut pour prendre en charge l’authentification fédérée. Dans ce cas, cette fonctionnalité peut être désactivée en créant la clé de Registre suivante pour autoriser les connexions à traverser.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server Gateway \\ preRDPDisableRegKey**

Lorsque cette clé existe, la passerelle Bureau à distance n’applique pas la redirection de l’appareil.

 

 




