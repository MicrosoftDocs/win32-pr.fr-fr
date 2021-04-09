---
title: Localisation d’un objet distant
description: Localisation d’un objet distant
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842806"
---
# <a name="locating-a-remote-object"></a>Localisation d’un objet distant

Avec l’avènement de COM pour les systèmes distribués, COM utilise le modèle de base pour la création d’objets décrit dans [objets de classe com et CLSID](com-class-objects-and-clsids.md) et ajoute plusieurs méthodes pour localiser un objet qui peut résider sur un autre système d’un réseau, sans surcharger l’application cliente.

COM a ajouté des clés de Registre qui permettent à un serveur d’enregistrer le nom de l’ordinateur sur lequel il réside ou sur l’ordinateur où se trouve un stockage existant. Par conséquent, les applications clientes doivent connaître uniquement le CLSID du serveur.

Toutefois, dans les cas où il est souhaité, COM a remplacé un paramètre précédemment réservé de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) par une structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , qui permet à un client de spécifier l’emplacement d’un serveur. Une autre valeur importante dans la fonction **CoGetClassObject** est l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , qui spécifie si l’objet attendu doit être exécuté in-process, local hors processus ou distant hors processus. Pris ensemble, ces deux valeurs et les valeurs dans le registre déterminent comment et où l’objet doit être exécuté.

> [!Note]  
> Les appels de création d’instance, lorsqu’ils spécifient un emplacement de serveur, peuvent remplacer un paramètre de registre. L’algorithme utilisé par COM pour ce faire est décrit dans la référence de l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .

 

L’activation à distance dépend de la relation de sécurité entre le client et le serveur. Pour plus d’informations, consultez [sécurité dans com](security-in-com.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de classe COM et CLSID](com-class-objects-and-clsids.md)
</dt> <dt>

[Création d’un objet à l’aide d’un objet de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 