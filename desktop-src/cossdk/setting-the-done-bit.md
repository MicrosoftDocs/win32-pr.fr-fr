---
description: Définition du bit terminé
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Définition du bit terminé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514543"
---
# <a name="setting-the-done-bit"></a>Définition du bit terminé

COM+ désactivera un objet activé juste-à-temps en fonction de l’état d’une propriété de contexte, le bit terminé, comme suit :

-   Lorsque le bit Done a la valeur true, COM+ désactive l’objet lors du retour de l’appel de la méthode en cours.
-   Lorsque le bit Done est défini sur false, l’objet reste actif lorsque l’appel de la méthode en cours est retourné.

Par défaut, le bit Done a la valeur false lorsqu’un objet est créé et que son contexte est initialisé. (Tout objet activé juste-à-temps est créé dans son propre contexte afin qu’il ait son propre bit terminé à définir.) Toutefois, vous pouvez modifier ce paramètre par défaut pour chaque méthode à l’aide de la propriété terminé automatiquement. Vous pouvez définir le bit Done des manières suivantes :

-   Utilisation de [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Utilisation de [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Utilisation de la propriété Done automatique

## <a name="using-icontextstate"></a>Utilisation de IContextState

Vous pouvez utiliser [**IContextState :: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) pour définir le bit Done sur true ou false.

Vous pouvez utiliser [**IContextState :: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) pour récupérer l’état actuel du bit Done à partir du contexte de l’objet.

## <a name="using-iobjectcontext"></a>Utilisation de IObjectContext

Vous pouvez utiliser les méthodes suivantes sur [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) pour définir le bit terminé tout en configurant simultanément le bit cohérent utilisé pour le vote dans les transactions :

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signale que vous avez terminé et que vous votez pour valider la transaction en cours. Il définit à la fois le bit Done et le bit consistent sur true.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signale que vous avez terminé et Dooms la transaction en cours. Elle définit le bit Done sur true et le bit cohérent sur false.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signale que vous n’avez pas terminé mais que vous votez pour valider la transaction. Elle définit le bit Done sur false et le bit cohérent sur true.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signale que vous n’avez pas terminé et que vous votez pour ne pas valider la transaction à ce stade, généralement parce que l’État est incohérent. Il définit à la fois le bit Done et le bit consistent sur false.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Mise en pool d’objets et activation JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transactions et activation JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



