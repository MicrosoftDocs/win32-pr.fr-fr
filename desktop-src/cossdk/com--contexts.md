---
description: Pour les composants configurés qui s’exécutent dans les applications COM+, les contextes constituent la base sur laquelle les services COM+ sont fournis.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contextes COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0ae1228f89797f9124e817db07f11a23dbec12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393180"
---
# <a name="com-contexts"></a>Contextes COM+

Pour les composants configurés qui s’exécutent dans les applications COM+, les *contextes* constituent la base sur laquelle les services com+ sont fournis. Dans COM+, un contexte est défini comme un ensemble de propriétés au moment de l’exécution associées à un ou plusieurs objets COM utilisés pour fournir des services pour ces objets.

Dans COM+, chaque objet COM est associé à un contexte exactement à mesure qu’il s’exécute (c’est-à-dire entre son activation et sa désactivation), et chaque contexte réside dans précisément un cloisonnement COM. Plusieurs objets peuvent s’exécuter dans le même contexte, et plusieurs contextes peuvent résider dans le même cloisonnement. Initialisé lorsqu’un objet est activé, les propriétés de contexte, telles que les propriétés de contexte de sécurité, représentent les besoins d’un objet au moment de l’exécution.

> [!Note]  
> Pour les composants non configurés qui n’utilisent pas les services COM+, le contexte est, pour l’essentiel, ignoré.

 

COM+ utilise des propriétés de contexte comme base pour fournir des services au moment de l’exécution. Ces propriétés contiennent l’État qui détermine la façon dont l’environnement d’exécution exécute des services pour les objets dans le contexte. Dans certains cas, vous pouvez interagir directement avec les propriétés de contexte d’un objet pour indiquer un État adapté à un service fourni pour l’objet. Par exemple, vous pouvez le faire lorsqu’un objet qui participe à une transaction automatique vote sur le résultat de la transaction.

Pour une présentation détaillée de la base COM de ces concepts, consultez [processus, threads et Apartments](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Interaction par programmation avec les propriétés de contexte

Chaque contexte est associé à un objet [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) qui effectue le suivi de ses propriétés. Vous pouvez accéder à **ObjectContext** en appelant la fonction [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) . Après avoir accédé à **ObjectContext**, vous pouvez appeler des méthodes sur l’interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) qu’il expose pour manipuler les propriétés de contexte.

Par exemple, l’appel de [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) a pour effet de définir le bit de cohérence de la transaction sur « consistent » et le bit d' [activation JIT](com--just-in-time-activation.md) sur « done » dans le contexte associé à l’objet. Des signaux « cohérents » vers COM+ que vous votez pour valider la transaction et « Done » indiquent que votre objet est prêt à être désactivé lorsque la méthode est retournée.

En plus de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext), d’autres interfaces spécialisées qui fournissent l’accès aux propriétés de contexte sont [**IObjectContextInfo**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo), [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)et [**IObjectContextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity). Dans une certaine mesure, [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) accède également aux propriétés de contexte. Vous pouvez utiliser [**IGetSecurityCallContext :: GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) pour obtenir **ISecurityCallContext**.

## <a name="understanding-activation-and-interception"></a>Compréhension de l’activation et de l’interception

En règle générale, vous devez réfléchir au contexte uniquement dans la mesure où il représente un certain nombre de propriétés, que vous pouvez définir ou obtenir, qui sont utilisées pour fournir des services COM+ pour vos composants. Dans certains cas, toutefois, vous devrez peut-être considérer les deux facettes de contextes suivantes de manière plus détaillée :

-   [Activation du contexte](context-activation.md)ou initialisation d’un objet dans un contexte approprié.
-   L' [interception](interception-of-cross-context-calls.md)ou ce que com+ effectue sur les appels à travers une limite de contexte.

## <a name="relation-to-mts-context-wrappers"></a>Relation avec les wrappers de contexte MTS

Les contextes remplacent efficacement les wrappers de contexte MTS. L’objectif qu’ils ont servi, à savoir fournir des services automatiques par le biais de demandes de création de recouvrement, est désormais une fonctionnalité intégrée de COM+. Par conséquent, vous n’avez plus besoin d’utiliser la fonction [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) . Dans MTS, **SafeRef** a été utilisé pour obtenir une référence à votre objet qui peut être passé en dehors de son Wrapper de contexte. Dans COM+, cela est inutile. des références d’objet normales (**ce** pointeurs) fonctionnent.

 

 
