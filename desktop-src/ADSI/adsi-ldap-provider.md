---
title: Fournisseur LDAP ADSI
description: Le fournisseur LDAP ADSI implémente un ensemble d’objets ADSI qui prennent en charge différentes interfaces ADSI. Pour accéder au fournisseur LDAP, établissez une liaison à l’un des objets ADSI LDAP, à l’aide de l’ADsPath LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Fournisseur LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9632f352bdfab9653de5c443d750be027c3dd74140c2a017e5d12a6dc0f673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180593"
---
# <a name="adsi-ldap-provider"></a>Fournisseur LDAP ADSI

Le fournisseur LDAP ADSI implémente un ensemble d’objets ADSI qui prennent en charge différentes interfaces ADSI. Pour accéder au fournisseur LDAP, établissez une liaison à l’un des objets ADSI LDAP, à l’aide de l’ADsPath LDAP.

Adsldp.dll, Adsldpc.dll, Adsmsext.dll et Activeds.dll doivent être installés sur votre ordinateur client pour fonctionner avec le fournisseur.

> [!Note]  
> Le fournisseur LDAP ADSI par défaut ne peut pas être considéré comme entièrement thread-safe. Les rédacteurs d’applications multithread doivent coordonner correctement l’accès entre les threads via l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.

 

 

 




