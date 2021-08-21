---
description: Dépannage
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Résolution des problèmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e10877306dc17f0b04718037a4bc073c8a7ed7c7c4ac46b31cda90517d22b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812005"
---
# <a name="troubleshooting"></a>Résolution des problèmes

Si vous rencontrez des problèmes pour diagnostiquer les erreurs de votre application, reportez-vous aux conseils de dépannage suivants :

-   Assurez-vous que le Distributed Transaction Coordinator (DTC) est en cours d’exécution sur tous les serveurs.
-   Vérifiez la communication réseau en commençant par le test sur un ordinateur local pour vérifier que l’application fonctionne. Si vous exécutez TCP/IP sur votre réseau, vous pouvez utiliser l’utilitaire ping.exe pour vérifier que les ordinateurs se trouvent sur le réseau.
-   assurez-vous que SQL et DTC se trouvent sur le même ordinateur ou que le programme de Configuration du Client dtc spécifie que le dtc se trouve sur un autre ordinateur. Si ce n’est pas le cas, SQLConnect renvoie une erreur en interne quand elle est appelée à partir d’un composant transactionnel.
-   Définissez le délai d’expiration de la transaction sur une valeur supérieure à la valeur par défaut de 60 secondes. Une fois que le délai d’expiration de la transaction s’est écoulé, COM+ abandonne la transaction. Tous les appels suivants au composant sont immédiatement retournés avec le contexte \_ E \_ abandonné.
-   Assurez-vous que vos pilotes ODBC sont thread-safe et n’ont pas d’affinité de thread.
-   Si vous avez des difficultés à faire fonctionner une application sur plusieurs serveurs, redémarrez le client, puis vérifiez que votre contrôleur de domaine est correctement configuré.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Recherche de la source d’une erreur](finding-the-source-of-an-error.md)
</dt> <dt>

[Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interprétation des codes d’erreur](interpreting-error-codes.md)
</dt> <dt>

[Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



