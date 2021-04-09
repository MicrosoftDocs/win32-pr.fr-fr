---
description: Vous pouvez configurer un composant à regrouper uniquement lorsqu’il est correctement écrit pour prendre en charge la mise en pool. Pour plus d’informations sur ces conditions requises, consultez Configuration requise pour les objets regroupables.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configuration d’un composant à regrouper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111447"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configuration d’un composant à regrouper

Vous pouvez configurer un composant à regrouper uniquement lorsqu’il est correctement écrit pour prendre en charge la mise en pool. Pour plus d’informations sur ces conditions requises, consultez [Configuration requise pour les objets regroupables](requirements-for-poolable-objects.md).

> [!Note]  
> Par défaut, un composant n’est pas configuré pour être regroupé.

 

Quand vous configurez un composant à regrouper, vous pouvez spécifier les propriétés suivantes pour déterminer comment COM+ gère le pool :

-   **Taille de pool minimale.** Représente le nombre d’objets qui sont créés lorsque l’application démarre et le nombre minimal d’objets qui sont conservés dans le pool pendant que l’application est en cours d’exécution. Si le nombre d’objets disponibles dans le pool descend en dessous de la valeur minimale spécifiée, les nouveaux objets sont créés pour répondre aux demandes d’objets en suspens et le rechargement du pool. Si le nombre d’objets disponibles dans le pool est supérieur au nombre minimal, ces objets excédentaires sont détruits au cours d’un cycle de nettoyage.
-   **Taille maximale du pool.** Représente le nombre maximal d’objets regroupés qui seront créés par le gestionnaire de regroupement, les deux étant activement utilisés par les clients et inactifs dans le pool. Lors de la création d’objets, le gestionnaire de regroupement vérifie que la taille maximale du pool n’a pas été atteinte et, si ce n’est pas le cas, le gestionnaire de pool crée une nouvelle instance de l’objet à distribuer au client. Si la taille maximale du pool a été atteinte, les demandes des clients seront mises en file d’attente et recevront le premier objet disponible du pool sur un premier servi. Les demandes de création d’objet expirent après une période spécifiée.
-   **Délai de création (MS).** Spécifie la durée d’attente d’un client, en millisecondes, pour qu’un objet soit retourné à partir du pool après un appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Si l’appel client échoue, le délai d’attente de l’erreur E \_ est retourné.

**Pour définir les propriétés liées au regroupement**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .

3.  Pour activer la mise en pool d’objets pour le composant, activez la case à cocher **activer le regroupement d’objets** .

4.  Dans la zone **taille minimale du pool** , entrez le nombre minimal d’objets de ce type dans le pool. Le pool est conservé pour avoir au moins ce nombre d’objets.

5.  Dans la zone u, entrez le nombre maximal d’objets de ce type dans le pool. Le nombre d’objets, activés et désactivés, ne dépassera jamais cette valeur.

6.  Dans la zone **délai de création (MS)** , entrez la durée, en millisecondes, pendant laquelle un client attendra un objet regroupé si celui-ci n’est pas immédiatement disponible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Analyse des statistiques des objets](monitoring-object-statistics.md)
</dt> </dl>

 

 
