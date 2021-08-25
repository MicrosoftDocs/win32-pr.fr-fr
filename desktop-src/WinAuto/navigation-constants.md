---
title: Constantes de navigation (oleacc. h)
description: Cette rubrique décrit les valeurs constantes, définies dans oleacc. h, qui indiquent le sens spatial (haut, bas, gauche et droit) ou logique (premier enfant, dernier, suivant et précédent) observé lorsque les clients utilisent IAccessible accNavigate pour naviguer d’un élément d’interface utilisateur à un autre dans le même conteneur.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e5c3a39c1b628ea03d1e036265ba7787e15bb70ce550e06b43b8efcd02c14a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998169"
---
# <a name="navigation-constants"></a>Constantes de navigation

Cette rubrique décrit les valeurs constantes, définies dans oleacc. h, qui indiquent le sens *spatial* (haut, bas, gauche et droit) ou *logique* (premier enfant, dernier, suivant et précédent) observé lorsque les clients utilisent [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) pour naviguer d’un élément d’interface utilisateur à un autre dans le même conteneur. Pour plus d’informations, consultez [Propriétés et méthodes de navigation entre les objets](object-navigation-properties-and-methods.md).

Les constantes de navigation Microsoft Active Accessibility sont les suivantes :



| Constante                                                                                                                                                                  | Description                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_**</dt> </dl>                   | Accédez à l’objet frère situé sous l’objet de départ.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ firstChild**</dt> </dl> | Naviguez jusqu’au premier enfant de cet objet. Lorsque cet indicateur est utilisé, le membre **lVal** du paramètre *VARSTART* doit être CHILDID \_ self.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LastChild**</dt> </dl>    | Naviguez jusqu’au dernier enfant de cet objet. Lors de l’utilisation de cet indicateur, le membre **lVal** du paramètre *VARSTART* doit être CHILDID \_ self.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR \_ gauche**</dt> </dl>                   | Accédez à l’objet frère situé à gauche de l’objet de départ.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ suivant**</dt> </dl>                   | Accédez à l’objet logique suivant ; en règle générale, il s’agit d’un frère de l’objet de départ.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ précédent**</dt> </dl>       | Accédez à l’objet logique précédent ; en règle générale, il s’agit d’un frère de l’objet de départ.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ droit**</dt> </dl>                | Accédez à l’objet frère situé à droite de l’objet de départ.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_**</dt> </dl>                         | Accédez à l’objet frère situé au-dessus de l’objet de départ.<br/>                                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



 

 





