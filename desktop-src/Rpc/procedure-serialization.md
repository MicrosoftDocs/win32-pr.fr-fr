---
title: Sérialisation de procédure
description: Lorsque vous utilisez la sérialisation de procédure, une procédure est étiquetée avec l’attribut \ encode \ ou \ Decode \. Au lieu de générer le stub distant habituel, le compilateur génère un stub de sérialisation pour la routine.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b514aa5a2e5be1b937a3989c3446bcc6e61c76f885381ce257286b5c625b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018949"
---
# <a name="procedure-serialization"></a>Sérialisation de procédure

Lorsque vous utilisez la sérialisation de procédure, une procédure est étiquetée avec l' \[ attribut [**encode**](/windows/desktop/Midl/encode) \] ou \[ [**Decode**](/windows/desktop/Midl/decode) \] . Au lieu de générer le stub distant habituel, le compilateur génère un stub de sérialisation pour la routine.

Tout comme une procédure distante doit utiliser un handle de liaison pour effectuer un appel distant, une procédure de sérialisation doit utiliser un handle de sérialisation pour utiliser les services de sérialisation. Si aucun handle de sérialisation n’est spécifié, un handle implicite par défaut est utilisé pour diriger l’appel. En revanche, si le handle de sérialisation est spécifié en tant qu’argument [**handle \_ t**](/windows/desktop/Midl/handle-t) explicite de la routine ou en utilisant l' \[ attribut [**\_ handle explicite**](/windows/desktop/Midl/explicit-handle) \] , vous devez passer un handle valide comme argument de l’appel. Pour plus d’informations sur la création d’un handle de sérialisation valide, consultez [Handles descripteurs](serialization-handles.md), [exemples d’encodage de mémoire tampon fixe](fixed-buffer-serialization.md)et [exemples d’encodage incrémentiel](examples-of-incremental-encoding.md).

> [!Note]
> Microsoft RPC permet le mélange des procédures distantes et de sérialisation dans une interface. Toutefois, soyez prudent quand vous le faites.
> 
> Pour les procédures distantes avec des handles de liaison implicites, le compilateur MIDL génère une variable de handle globale de type [**handle \_ t**](/windows/desktop/Midl/handle-t). Les procédures et les types avec des handles de sérialisation implicites utilisent cette même variable de handle global.
> 
> Pour les handles implicites, le handle global implicite doit être défini sur un handle de liaison valide avant un appel distant. Le handle implicite doit être défini sur un handle de sérialisation valide avant un appel de sérialisation. Par conséquent, une procédure ne peut pas être à la fois à distance et sérialisée. Il doit s’agir de l’un ou de l’autre.

 

 

 