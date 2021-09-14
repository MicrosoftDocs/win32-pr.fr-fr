---
description: Configuration de la stratégie de restriction logicielle
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configuration de la stratégie de restriction logicielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916828"
---
# <a name="configuring-the-software-restriction-policy"></a>Configuration de la stratégie de restriction logicielle

Lorsque vous définissez explicitement les niveaux de confiance de la stratégie de restriction logicielle d’une application COM+, vous remplacez les paramètres par défaut du système. Cela est souvent nécessaire pour les applications serveur COM+, car le niveau de confiance du système est défini de façon identique pour toutes les applications serveur (car elles s’exécutent toutes dans le même fichier, dllhost.exe). Toutefois, lorsque vous définissez le niveau de confiance de la stratégie de restriction logicielle d’une application de bibliothèque COM+, vous affectez la configuration du système pour cette application. Pour plus d’informations sur l’utilisation de la stratégie de restriction logicielle dans COM+, consultez [utilisation de la stratégie de restriction logicielle dans com+](using-the-software-restriction-policy-in-com-.md).

**Pour définir la stratégie de restriction logicielle**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous définissez la stratégie de restriction logicielle, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Sous **stratégie de restriction logicielle**, activez la case à cocher **appliquer la stratégie de restriction logicielle** . Cela vous permet de définir le niveau de confiance. Si vous désactivez la case à cocher, COM+ utilise la configuration du système de la stratégie de restriction logicielle pour l’application. Cette case à cocher correspond à la propriété SRPEnabled de la collection d' [**applications**](applications.md) .

4.  Dans la zone **niveau de restriction** , sélectionnez le niveau approprié. Cette zone de liste déroulante correspond à la propriété SRPTrustLevel de la collection d' [**applications**](applications.md) . Les niveaux sont les suivants, classés du moins au plus fiable :

    -   **Interdit**. L’application n’est pas autorisée à utiliser les privilèges complets de l’utilisateur. Les composants avec n’importe quel niveau de confiance peuvent être chargés dans celui-ci.
    -   Non **restreint**. L’application dispose d’un accès illimité aux privilèges de l’utilisateur. Seuls les composants avec un niveau de confiance non restreint peuvent être chargés dans celui-ci.

5.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de la sécurité de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Définition d’un niveau d’authentification pour une application serveur](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Définition d’un niveau d’emprunt d’identité](setting-an-impersonation-level.md)
</dt> </dl>

 

 



