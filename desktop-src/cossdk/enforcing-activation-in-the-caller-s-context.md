---
description: Application de l’activation dans le contexte des appelants
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Application de l’activation dans le contexte des appelants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514739"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Application de l’activation dans le contexte de l’appelant

Vous pouvez contrôler si un objet est activé dans son propre contexte. Lorsque vous utilisez l’outil d’administration Services de composants pour exiger l’activation d’un composant dans le contexte de l’appelant, les opérations suivantes se produisent lorsque COM+ active une instance du composant dans un contexte :

-   L’objet est activé dans le contexte du créateur, si possible.
-   L’activation d’objet échoue si elle requiert son propre contexte ; CO \_ E \_ tentative \_ de \_ création d’un \_ \_ contexte client externe \_ est retourné.

Le fait que l’objet nécessite ou non son propre contexte dépend de sa configuration par rapport à l’état actuel des propriétés de contexte de l’appelant. Pour plus d’informations, consultez [contextes com+](com--contexts.md).

Vous souhaitez contrôler l’activation à un niveau précis si certains aspects de votre objet ne fonctionneront pas correctement s’ils ont son propre contexte. Par exemple, si le composant ne prend pas en charge le marshaling et qu’il a son propre contexte, tous les appels à ce dernier échouent, car les appels entre les contextes sont interceptés et un marshaling léger effectué.

**Pour appliquer l’activation dans le contexte de l’appelant**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant (situé dans le dossier **composants** de n’importe quelle application com+ sélectionnée) pour lequel vous définissez les propriétés d’activation, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .

3.  Activez la case à cocher **doit être activé dans le contexte des appelants** .

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts d’activation juste-à-temps de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Application de l’activation dans le contexte par défaut](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



