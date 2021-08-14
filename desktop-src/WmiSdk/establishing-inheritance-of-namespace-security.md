---
description: Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Établissement de l’héritage de la sécurité des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951bd5a2a14aa0a62620090d07df9bc56e8a0832674f2c1eee84369f4e2b4dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411909"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Établissement de l’héritage de la sécurité des espaces de noms

Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.

Les espaces de noms WMI ont des descripteurs de sécurité qui contrôlent qui peut accéder à l’espace de noms et aux données de l’espace de noms. Chaque descripteur de sécurité a une liste de contrôle d’accès discrétionnaire (DACL) et une liste de contrôle d’accès de sécurité (SACL). Ces listes contiennent des entrées de contrôle d’accès (ACE).

En fonction des [**constantes d’indicateur d’entrée**](namespace-ace-flag-constants.md) du contrôle d’accès de l’espace de noms définies, les autorisations appliquées à un espace de noms peuvent être héritées par tous les espaces de noms enfants de cet espace de noms. Un espace de noms enfant hérite du descripteur de sécurité de son espace de noms parent lorsque l’espace de noms enfant est créé si l’indicateur **\_ \_ ACE inherit du conteneur** se trouve dans le descripteur de sécurité de l’espace de noms parent. Si le **conteneur hérite de l’entrée de contrôle d’accès, l’entrée de contrôle d’accès n’hérite pas \_ \_ \| \_ se propager \_ \_** est définie. Les espaces de noms enfants peuvent remplacer les autorisations de sécurité de leur parent en appelant des méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) pour écrire un nouveau descripteur de sécurité. Les paramètres de sécurité par défaut ne peuvent pas être modifiés. Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md). Pour plus d’informations sur les DACL, consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [**constantes de type ACE d’espace de noms**](namespace-ace-type-constants.md).

Notez que les autorisations par défaut ne peuvent pas être modifiées. en outre, la définition de la SE indicateur de **\_ \_ protection DACL** lors de la définition du descripteur de sécurité (sd) n’est pas utilisé pour ajouter un sd spécialisé à un espace de noms enfant. Pour remplacer un SD hérité, il vous suffit d’en définir un nouveau. Pour hériter de ce SD sur un espace de noms enfant, transmettez l’indicateur **\_ \_ ACE inherit au conteneur** dans le descripteur de sécurité de l’espace de noms. Pour hériter uniquement de l’enfant, et non des descendants, passer `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
