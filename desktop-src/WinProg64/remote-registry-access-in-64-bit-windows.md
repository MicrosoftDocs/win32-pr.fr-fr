---
title: Accès au Registre distant dans Windows 64 bits
description: Le redirecteur du Registre fournit un accès à distance au registre sur Windows 64 bits via la fonction RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- accès au registre à distance, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106540764"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Accès au Registre distant dans Windows 64 bits

Le redirecteur du Registre fournit un accès à distance au registre sur Windows 64 bits via la fonction [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Si le client est une application 32 bits, il accède à la vue de Registre 32 bits par défaut du serveur. Si le client est une application 64 bits, il accède à la vue de Registre 64 bits.

**Windows Server 2003 :** Tous les clients accèdent à la vue de Registre 64 bits, sauf si l’application utilise l’indicateur de clé \_ WOW64 \_ 32KEY. Ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1) et Windows XP Professionnel Édition x64, à condition que le client et le serveur exécutent ces versions de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redirecteur du Registre](registry-redirector.md)
</dt> <dt>

[Réflexion du Registre](registry-reflection.md)
</dt> </dl>

 

 