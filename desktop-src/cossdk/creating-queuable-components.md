---
description: Un composant avec au moins une interface de mise en file d’attente est un composant de mise en file d’attente.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Création de composants de mise en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ca7b4717da44145121508ed3e8b208e8401a240f1a2ceb858be299bf2b32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637839"
---
# <a name="creating-queuable-components"></a>Création de composants de mise en file d’attente

Un composant avec au moins une interface de mise en file d’attente est un composant de mise en *file d’attente*. Pour qu’un composant soit appelé par une file d’attente, les interfaces doivent être marquées comme étant en file d’attente et le composant doit être installé dans une application en file d’attente. Toutefois, un composant pouvant être mis en file d’attente peut être un composant d’une application qui n’est pas en file d’attente.

Une interface de mise en file d’attente ne doit contenir que des paramètres in, aucun paramètre de sortie ni aucune valeur de retour. Ces caractéristiques sont vérifiées en analysant les informations de type lors de l’installation du composant. Si l’interface n’est pas mise en file d’attente, la file d’attente de l’application contenant le composant ne peut pas être activée.

Pour spécifier une interface COM+ en tant que file d’attente, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Ouvrez le dossier **interfaces** du composant de l’application com+ que vous souhaitez mettre en file d’attente.

3.  Cliquez avec le bouton droit sur l’interface que vous souhaitez marquer comme étant en file d’attente, puis cliquez sur **Propriétés**.

4.  Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.

5.  Activez la case à cocher intitulée en **attente**.

    > [!Note]  
    > Si la case à cocher en file d’attente est grisée, l’interface ne satisfait pas aux contraintes de mise en **file d’attente** décrites ci-dessus.

     

6.  Cliquez sur **OK**.

    Un composant pouvant être mis en file d’attente peut être identifié en tant que tel, en ajoutant la macro d’attribut QUEUEable à la section interface du fichier source IDL (Interface Definition Language) pour toutes les interfaces qui peuvent être mises en file d’attente.

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de files d’attente de composants](creating-component-queues.md)
</dt> <dt>

[Développement de composants en file d’attente](developing-queued-components.md)
</dt> </dl>

 

 



