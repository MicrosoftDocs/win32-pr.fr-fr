---
title: Fournisseur LDAP ADSI
description: Le fournisseur LDAP ADSI implémente un ensemble d’objets ADSI qui prennent en charge différentes interfaces ADSI. Pour accéder au fournisseur LDAP, établissez une liaison à l’un des objets ADSI LDAP, à l’aide de l’ADsPath LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Fournisseur LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839245"
---
# <a name="adsi-ldap-provider"></a>Fournisseur LDAP ADSI

Le fournisseur LDAP ADSI implémente un ensemble d’objets ADSI qui prennent en charge différentes interfaces ADSI. Pour accéder au fournisseur LDAP, établissez une liaison à l’un des objets ADSI LDAP, à l’aide de l’ADsPath LDAP.

Adsldp.dll, Adsldpc.dll, Adsmsext.dll et Activeds.dll doivent être installés sur votre ordinateur client pour fonctionner avec le fournisseur.

> [!Note]  
> Le fournisseur LDAP ADSI par défaut ne peut pas être considéré comme entièrement thread-safe. Les rédacteurs d’applications multithread doivent coordonner correctement l’accès entre les threads via l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.

 

 

 




