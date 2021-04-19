---
description: Vous pouvez activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par un composant pour lequel l’activation JIT COM+ est activée. Si l’activation JIT est désactivée, la saisie semi-automatique n’est pas disponible.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Activation de la saisie semi-automatique pour une méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543446"
---
# <a name="enabling-auto-done-for-a-method"></a>Activation de la saisie semi-automatique pour une méthode

Vous pouvez activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par un composant pour lequel l’activation JIT COM+ est activée. Si l’activation JIT est désactivée, la saisie semi-automatique n’est pas disponible.

Vous devez activer la saisie semi-automatique uniquement pour une méthode qui a intentionnellement été écrite pour en tirer parti, car cette fonctionnalité peut potentiellement modifier le comportement attendu de la méthode.

Lorsque vous activez l’option automatique, vous modifiez le comportement par défaut de l’activation JIT et des transactions automatiques pour cette méthode. Vous pouvez utiliser cette fonctionnalité, car elle peut supprimer la nécessité de déclarer explicitement la cohérence et le fait. Pour ce faire, il suffit de retourner un HRESULT lorsque l’option auto-Done est activée. Pour l’essentiel, lorsque vous activez l’exécution automatique, vous demandez à COM+ d’effectuer les opérations suivantes :

-   Définissez le bit Done sur true par défaut dans le contexte dans lequel l’objet s’exécute chaque fois que cette méthode est appelée.
-   Inspectez le HRESULT retourné par la méthode. Si elle indique la réussite ou l’échec, définissez le bit de cohérence en conséquence. Cela peut entraîner un appel automatique à [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), en fonction également de ce que fait la méthode en interne.

**Pour activer la saisie semi-automatique pour une méthode**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur la méthode que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de la méthode, cliquez sur l’onglet **général** .

3.  Pour activer la saisie semi-automatique, activez la case à cocher **désactiver automatiquement cet objet lorsque cette méthode est retournée** . Si la case à cocher n’est pas disponible, vous devez d’abord activer l’activation JIT pour le composant. (Pour obtenir des instructions détaillées, consultez[activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md) .)

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Définition du bit terminé](setting-the-done-bit.md)
</dt> </dl>

 

 



