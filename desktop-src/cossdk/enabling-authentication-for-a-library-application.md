---
description: Activation de l’authentification pour une application de bibliothèque
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Activation de l’authentification pour une application de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb3d5799ee8fac1d8eb266e6513c4d2a759adb10b78b2117424b08f8c5d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736418"
---
# <a name="enabling-authentication-for-a-library-application"></a>Activation de l’authentification pour une application de bibliothèque

Étant donné que les applications de bibliothèque COM+ sont hébergées par d’autres processus, leurs exigences de sécurité peuvent être différentes de celles des applications serveur. Si l’application de bibliothèque doit être hébergée par un navigateur, il peut être nécessaire de recevoir des rappels non authentifiés.

Pour répondre à ce besoin, vous pouvez désactiver l’authentification afin que le processus d’hébergement n’effectue pas de vérifications de sécurité pour les appelants de l’application de bibliothèque. Lorsque vous désactivez l’authentification, les appels à l’application de la bibliothèque ne sont pas authentifiés, mais tous les appels à ce dernier sont correctement effectués. Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).

**Pour activer (ou désactiver) l’authentification pour une application de bibliothèque**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous activez ou désactivez l’authentification, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Sous **authentification**, activez la case à cocher **activer l’authentification** pour activer l’authentification. la désactivation de la case à cocher désactive l’authentification.

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition d’un niveau d’authentification pour une application serveur](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



