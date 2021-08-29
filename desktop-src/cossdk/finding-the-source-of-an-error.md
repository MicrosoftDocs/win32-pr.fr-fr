---
description: Recherche de la source d’une erreur
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Recherche de la source d’une erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368f67294491148f9bc85b04ca02ab8e3707eb316261ea50138d7b9c356a2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954079"
---
# <a name="finding-the-source-of-an-error"></a>Recherche de la source d’une erreur

Vous pouvez diagnostiquer la source et obtenir une description des erreurs d’application à l’aide de COM+ et d’autres outils. si vous découvrez que l’erreur d’application est provoquée par COM+, vous pouvez interpréter le message d’erreur qui affiche le fichier Winerror. h ou à l’aide de l’utilitaire Microsoft Visual C++ error.

Si votre application serveur échoue ou provoque un comportement inattendu, vous devez d’abord déterminer l’emplacement où l’erreur s’est produite. Le système observateur d’événements effectue le suivi des événements de l’application, de la sécurité et du système. De nombreuses erreurs « silencieuses » sont enregistrées ici. Toutefois, toutes les erreurs ne sont pas affichées dans la observateur d’événements.

Vous devez d’abord faire référence au journal des applications dans le observateur d’événements pour vérifier l’application associée au message d’événement. (Étant donné que vous pouvez également archiver les journaux des événements, vous pouvez suivre l’historique des événements de l’erreur.) Double-cliquez sur une entrée dans votre journal pour activer une page de **propriétés d’événement** qui fournit des informations supplémentaires sur l’événement système.

Pour plus d’informations sur le débogage d’une application COM+, consultez [débogage d’applications com+](debugging-com--applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interprétation des codes d’erreur](interpreting-error-codes.md)
</dt> <dt>

[Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Dépannage](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



