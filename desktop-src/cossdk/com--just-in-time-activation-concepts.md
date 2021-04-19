---
description: Le service d’activation juste-à-temps (JIT) permet à COM+ de désactiver un objet alors qu’un client contient toujours une référence active à cet objet.
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: Concepts d’activation juste-à-temps de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513924"
---
# <a name="com-just-in-time-activation-concepts"></a>Concepts d’activation juste-à-temps de COM+

Le service d’activation juste-à-temps (JIT) permet à COM+ de désactiver un objet alors qu’un client contient toujours une référence active à cet objet. La prochaine fois que le client appelle une méthode sur l’objet, que le client estime toujours actif, le service d’activation JIT COM+ réactive l’objet de manière transparente au client, juste à temps.

Le principal avantage de l’utilisation de COM + l’activation JIT est que vous pouvez permettre aux clients de conserver des références aux objets aussi longtemps qu’ils en ont besoin, sans nécessairement mettre en place des ressources serveur précieuses telles que la mémoire. Les autres avantages importants sont les suivants :

-   L’utilisation du service d’activation JIT COM+ simplifie grandement le modèle de programmation pour le client, car le client n’a pas à réfléchir à la façon dont il utilise des objets serveur et des ressources serveur coûteux. Sans l’activation JIT, les clients peuvent subir une pénalité significative lorsqu’ils ont souvent besoin d’appeler et de libérer des objets.
    > [!Note]  
    > Vous pouvez affiner ce gain de performances en utilisant le service de mise en [pool d’objets com+](com--object-pooling.md) . En regroupant les objets activés par le JIT, vous pouvez considérablement accélérer la réactivation des objets pour les clients tout en réutilisant les ressources qu’ils peuvent contenir, ce qui vous permet de contrôler plus précisément la quantité de mémoire utilisée par un objet donné sur le serveur. Pour plus d’informations, consultez mise en [pool d’objets et activation JIT com+](object-pooling-and-com--jit-activation.md).

     

-   Avec les applications distribuées, un aller-retour réseau onéreux est nécessaire pour la création de chaque objet, et plus le client est éloigné du serveur, plus les coûts d’activation et de marshaling de l’objet serveur, d’ouverture du canal et de configuration du proxy et du stub sont importants. En utilisant le service d’activation JIT COM+, vous pouvez réduire la fréquence de création des objets pour améliorer de manière significative les performances de votre application.
-   Lorsque vous utilisez l’activation JIT COM+ pour activer les objets sur lesquels les clients contiennent des références à long terme, mais qui ne sont pas nécessairement utilisées tout le temps, la mémoire du serveur n’est pas toujours liée à la conservation de ces objets actifs. Cela peut augmenter considérablement l’évolutivité de votre application. Le seul impact sur les performances que les clients voient est le temps qu’il faut pour réactiver l’objet, généralement plus de temps qu’il n’en faut pour allouer de la mémoire pour l’objet et sensiblement inférieur à l’aller-retour réseau pour la création de l’objet distant.

## <a name="enabling-com-jit-activation"></a>Activation de l’activation JIT COM+

Vous pouvez activer le service d’activation JIT COM+ pour un composant à l’aide de l’outil d’administration Services de composants ou des fonctions d’administration. Pour plus d’informations sur la façon de procéder, consultez [activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md).

L’activation JIT COM+ peut interagir avec d’autres services COM+, tels que les suivants :

-   Lorsque votre composant requiert des transactions, l’activation JIT est automatiquement activée pour celle-ci. Pour plus d’informations, consultez [transactions et activation JIT com+](transactions-and-com--jit-activation.md).
-   Lorsque votre composant est activé pour l’activation juste-à-temps, la synchronisation est automatiquement définie sur obligatoire. Cela signifie que si deux clients appellent simultanément un composant activé juste-à-temps et un appel de méthode pour l’un d’eux retourne, ce qui entraîne la désactivation de l’objet, l’autre n’est pas laissée bloquée.

## <a name="how-deactivation-is-triggered"></a>Mode de déclenchement de la désactivation

COM+ désactive un objet en fonction de l’état du bit de réalisation sur le contexte de l’objet. Votre objet peut utiliser ce bit pour signaler s’il est terminé (c’est-à-dire prêt à être désactivé) pendant un appel de méthode donné. Pour plus d’informations, consultez [définition du bit terminé](setting-the-done-bit.md).

## <a name="using-the-auto-done-property"></a>Utilisation de la propriété Done automatique

À l’aide de l’outil d’administration Services de composants, vous pouvez configurer une méthode de sorte que l’objet soit automatiquement désactivé lors du retour de la méthode. (Pour obtenir des instructions sur la définition de cette propriété, consultez [activation de la saisie semi-automatique pour une méthode](enabling-auto-done-for-a-method.md) .) En sélectionnant cette option, vous pouvez éliminer les appels de méthode répétitifs pour voter dans les transactions. Étant donné que le paramètre par défaut pour le bit de cohérence a la valeur true, si vous avez également modifié le bit Done en true et que vous n’effectuez aucune action pour modifier ces paramètres, [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) est appelé automatiquement après le retour de la méthode.

Toutefois, il existe un inconvénient à ce comportement : COM+ examine le HRESULT retourné par la méthode. Si cette valeur HRESULT indique un échec, le bit de cohérence est défini sur false et le résultat est le même que si vous aviez appelé [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

Pour résumer, si vous sélectionnez terminé automatiquement pour une méthode et que vous n’effectuez aucune action pour définir des bits, et si un HRESULT (HR) est retourné, les conditions suivantes s’appliquent :

-   Si la méthode est réussie (HR), c’est comme si vous appeliez [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete).
-   En cas d’échec (HR), c’est comme si vous appeliez [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>Utilisation de IObjectControl pour gérer l’activation et la désactivation d’objets

Vous pouvez implémenter l’interface [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) afin que le runtime com+ gère automatiquement la désactivation et la réactivation de vos objets. Lorsqu’un objet implémente cette interface, COM+ appelle [**IObjectControl ::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) quand il désactive l’objet et [**IObjectControl :: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) lorsqu’il le réactive. Ces méthodes activent l’initialisation de contexte automatique sur l’activation d’objet et le nettoyage de l’État sur la désactivation.

Si vous regroupez des objets qui utilisent l’activation JIT COM+, il est vivement recommandé d’implémenter [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Pour plus d’informations, consultez mise en [pool d’objets et activation JIT com+](object-pooling-and-com--jit-activation.md).

## <a name="statelessness-and-jit-activation"></a>Abandon et activation JIT

Les objets transactionnels sont nécessairement sans État, car vous ne pouvez pas partager l’État à travers une limite de transaction. Par conséquent, vous devez utiliser l’activation juste-à-temps uniquement lorsque votre objet ne contient aucun État qui serait perdu lors de la désactivation. dans le cas contraire, vous ne respectez pas l’isolation des transactions. En raison des modèles d’utilisation naturelle des objets transactionnels, ils effectuent une certaine unité de travail et libèrent l’objet lorsque la transaction est validée ou abandonnée : l’activation juste-à-temps et les transactions automatiques sont étroitement liées. La configuration d’un objet pour exiger des transactions active automatiquement COM+ JIT activation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches d’activation juste-à-temps COM+](com--just-in-time-activation-tasks.md)
</dt> <dt>

[Mise en pool d’objets et activation JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transactions et activation JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



