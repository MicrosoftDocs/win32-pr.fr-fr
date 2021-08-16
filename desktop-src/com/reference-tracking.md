---
title: Suivi des références
description: Suivi des références
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1321c922cc0a7493e3e4792f7c0f925618330c2e42665296fb06792635a4ea70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309762"
---
# <a name="reference-tracking"></a>Suivi des références

Le suivi de référence peut empêcher la version antérieure involontaire ou malveillante d’objets.

Lorsque vous activez le suivi des références, vous demandez que les appels de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribués soient authentifiés par com. Lorsque le suivi de référence est activé, COM effectue le suivi du nombre de références par utilisateur afin qu’un utilisateur puisse appeler **Release** uniquement sur les objets sur lesquels l’utilisateur a précédemment appelé **AddRef** . Bien que le suivi de référence puisse réduire les performances, il garantit que, quel que soit le nombre de fois où un utilisateur donné appelle **Release**, les objets et les stubs existent toujours si une autre personne y fait référence.

Le client peut définir le suivi de référence pour un processus en passant l' \_ indicateur de fonctionnalité EOAC Secure \_ REFS dans un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Vous pouvez également activer ou désactiver le suivi des références pour toutes les applications sur un ordinateur à l’aide de Dcomcnfg.exe.

Si le suivi de référence est activé, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) utilise toujours les paramètres de sécurité par défaut. Dans ce cas, les appels à [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur **IUnknown** échouent.

 

 