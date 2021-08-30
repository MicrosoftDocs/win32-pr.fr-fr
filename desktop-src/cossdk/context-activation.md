---
description: Dans COM+, chaque objet COM est créé avec un contexte associé.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Activation du contexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab785040e6cf28b609fe80d4160da90bd3fe640b2229cf982993c8573378e4bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096849"
---
# <a name="context-activation"></a>Activation du contexte

Dans COM+, chaque objet COM est créé avec un contexte associé. Cela signifie qu’un nouveau contexte doit être créé et initialisé ou qu’un contexte existant approprié est utilisé. Ce processus est appelé *activation*. Dans COM+, un objet est activé dans son propre contexte ou dans celui de son créateur (un objet qui a demandé l’activation de l’objet, par exemple, en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)).

Dans certains cas, par exemple avec le [regroupement d’objets](com--object-pooling.md), un objet est activé sans être créé à partir de zéro. Dans ce cas, une instance en cours d’exécution est activée dans un contexte. Pendant sa durée de vie, il peut être activé à plusieurs reprises dans différents contextes.

Le mécanisme de base est le même dans les deux cas : un objet est associé à un contexte et ce contexte est correctement initialisé pour représenter les besoins de l’objet au moment de l’exécution.

## <a name="flowing-of-context-properties"></a>Déplacement des propriétés de contexte

Lorsqu’un objet est activé en réponse à une demande de création d’un autre objet, COM+ doit effectuer un médiateur entre eux pour activer correctement l’objet en aval. COM+ doit comparer le contexte de l’appelant avec la configuration du composant appelé, puis décider où activer le composant en aval et comment initialiser ses propriétés de contexte.

Pour découvrir la configuration du composant, COM+ le recherche dans la base de données d’inscription de classe COM+, qui est optimisée pour les recherches à temps d’exécution extrêmement rapides. (Cela est déterminé par la façon dont vous avez configuré un composant lors de son installation dans une application COM+.) La configuration du composant est ensuite examinée par rapport à l’état des propriétés de contexte de l’appelant.

Dans certains cas, la configuration est cohérente avec le contexte de l’appelant et le composant peut être activé dans le contexte de l’appelant. Cela peut se produire uniquement si le contexte de l’appelant remplit toutes les conditions d’exécution du nouvel objet.

Lorsque le composant en aval ne peut pas être activé dans le contexte de l’appelant, il est activé dans son propre contexte dans un cloisonnement approprié. Lorsque cela se produit, certaines propriétés de contexte peuvent être acheminées de l’appelant vers l’appelé. Par exemple, si l’appelant est associé à une transaction et que l’appelé prend en charge les transactions, le nouvel objet obtient son propre contexte (pour voter dans la transaction, il doit avoir son propre indicateur cohérent) et hérite de l’ID de transaction et de l’ID d’activité de l’appelant (qui se trouvent dans la même transaction et le même domaine de synchronisation).

## <a name="ignored-context-properties"></a>Propriétés de contexte ignorées

En fonction du mode de configuration d’un composant, certaines propriétés de contexte peuvent ne jouer aucun rôle pour déterminer si elles sont activées dans le contexte du créateur ou dans son propre contexte. Par exemple, les paramètres transactions désactivées et synchronisation désactivée, indiquant la présence d’une transaction ou d’un domaine de synchronisation, ne joueront aucun rôle dans l’activation du composant. Ces propriétés sont ignorées de façon fondamentale lorsque le contexte est transmis. Si un composant utilise uniquement la vérification de l’accès au niveau du processus, sa propriété de contexte de sécurité est ignorée ; la configuration de sécurité du composant ne joue jamais un rôle dans son activation.

## <a name="forcing-activation-in-the-callers-context"></a>Forcer l’activation dans le contexte de l’appelant

Dans certains cas, vous souhaiterez peut-être activer un objet uniquement dans le contexte de son appelant, autrement dit, jamais activé dans son propre contexte. Par exemple, vous souhaiterez peut-être contrôler le comportement de l’objet lorsqu’il est appelé sur une limite de contexte.

Vous pouvez vous assurer qu’un objet ne peut pas être activé dans son propre contexte en sélectionnant l’option **doit être activé dans le contexte des appelants** sous l’onglet **activation** de la page **Propriétés** du composant, à l’aide de l’outil d’administration Services de composants. (Pour obtenir des instructions pas à pas, consultez [application de l’activation dans le contexte de l’appelant](enforcing-activation-in-the-caller-s-context.md) .) Lorsque vous sélectionnez cette option, si l’objet ne peut pas être activé dans le contexte de l’appelant, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) échoue et retourne co \_ E \_ tentative \_ de création d’un \_ \_ \_ contexte client extérieur \_ .

## <a name="default-context"></a>Contexte par défaut

Les contextes par défaut existent pour prendre en charge les composants non configurés, c’est-à-dire les composants COM qui ne sont pas installés dans les applications COM+ et qui ne sont pas enregistrés dans la base de données d’inscription de classe COM+. Si les composants non configurés ont un modèle de thread compatible, ils sont activés dans le contexte de l’appelant. Dans le cas contraire, ils sont activés dans un contexte par défaut dans le cloisonnement approprié. Chaque cloisonnement a un contexte par défaut pour prendre en charge les objets COM qui n’utilisent pas les services COM+.

## <a name="hooking-activation"></a>Activation du raccordement

En implémentant [**IObjectControl :: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) et [**IObjectControl ::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), vous pouvez raccorder l’activation et la désactivation ensemble pour effectuer une initialisation spéciale dans le nouveau contexte. Ces méthodes sont appelées par COM+ à certains stades du cycle de vie d’un objet, lorsque l’objet est configuré pour utiliser l’activation JIT ou le regroupement d’objets. Pour plus d’informations, consultez [activation juste-à-temps de com+](com--just-in-time-activation.md) et mise en [pool d’objets com+](com--object-pooling.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interception d’appels entre les contextes](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
