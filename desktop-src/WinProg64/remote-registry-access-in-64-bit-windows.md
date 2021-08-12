---
title: Accès au registre à distance en Windows 64 bits
description: le redirecteur du registre fournit un accès à distance au registre sur le Windows 64 bits via la fonction RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- accès au registre à distance 64-bit Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561450"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Accès au registre à distance en Windows 64 bits

le redirecteur du registre fournit un accès à distance au registre sur le Windows 64 bits via la fonction [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Si le client est une application 32 bits, il accède à la vue de Registre 32 bits par défaut du serveur. Si le client est une application 64 bits, il accède à la vue de Registre 64 bits.

**Windows Server 2003 :** Tous les clients accèdent à la vue de Registre 64 bits, sauf si l’application utilise l’indicateur de clé \_ WOW64 \_ 32KEY. ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1) et Windows XP Professional édition x64, à condition que le client et le serveur exécutent ces versions de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redirecteur du Registre](registry-redirector.md)
</dt> <dt>

[Réflexion du Registre](registry-reflection.md)
</dt> </dl>

 

 