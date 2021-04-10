---
title: Sécurité Server-Side
description: Sécurité Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941401"
---
# <a name="server-side-security"></a>Sécurité Server-Side

Le serveur peut récupérer des informations de sécurité sur un appelant ou emprunter l’identité de l’appelant à l’aide des méthodes de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). Une implémentation de **IServerSecurity** est fournie par com sur l’objet de contexte pour l’appel actuel lorsque le marshaling standard est utilisé. Toutefois, cette interface peut être absente pour certaines interfaces marshalées personnalisées.

Lorsqu’un appel arrive sur le serveur, le serveur peut appeler [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) pour obtenir un pointeur vers l’interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) . Avec ce pointeur, les méthodes **IServerSecurity** peuvent être appelées par le serveur pour connaître les paramètres d’authentification du client et pour emprunter l’identité du client, si nécessaire. L’objet **IServerSecurity** est valide sur n’importe quel thread du cloisonnement jusqu’à ce que l’appel représenté par **IServerSecurity** se termine. Pour plus d’informations sur l’emprunt d’identité, consultez [emprunt d’identité](impersonation.md) et [masquage](cloaking.md).

Les fonctions d’assistance suivantes qui reposent sur l’implémentation de l’interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) de l’objet de contexte d’appel sont également disponibles :

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 