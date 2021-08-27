---
description: Server-Side la configuration requise pour l’emprunt d’identité
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side la configuration requise pour l’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e43016428f2ff083fc5a783d05c3c79e241dcf299f3af9ca226cb4f6a2cf1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096799"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side la configuration requise pour l’emprunt d’identité

Le serveur effectue l’emprunt d’identité par programmation. Il suppose explicitement les informations d’identification de sécurité du client à l’aide de [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Lorsque le client a accordé au serveur une autorité suffisante, cela a pour effet de remplacer les informations d’identification de sécurité du client par le jeton de thread du serveur, à la place du jeton de processus.

Une fois cette opération effectuée, le serveur peut, par exemple, utiliser le jeton client pour accéder aux ressources protégées par un descripteur de sécurité. Ou elle peut effectuer des appels sous l’identité du client, si le masquage est activé.

Le serveur peut explicitement définir le masquage par programme, ou il peut s’appuyer sur un paramètre d’administration. Par défaut, les applications COM+ sont configurées pour utiliser le masquage dynamique. Pour plus d’informations, consultez [masquage](cloaking.md).

Si le serveur implémente la délégation pour le compte du client (à l’aide de l’identité du client sur le réseau), l’identité du processus serveur doit être marquée comme « approuvée pour la délégation » dans le service Active Directory ; dans le cas contraire, la délégation échouera.

Lorsqu’il a terminé d’utiliser l’identité du client, le serveur peut revenir à son propre jeton de processus à l’aide de [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).

Pour plus d’informations sur l’implémentation de l’emprunt d’identité et de la délégation, consultez [délégation et emprunt d’identité](/windows/desktop/com/delegation-and-impersonation).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Exigences côté client pour l’emprunt d’identité](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Masquer](cloaking.md)
</dt> </dl>

 

 
