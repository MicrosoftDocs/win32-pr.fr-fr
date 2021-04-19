---
description: La liste suivante répertorie les valeurs possibles du champ indicateurs dans une entrée de Access Control WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes d’indicateur d’ACE d’espace de noms (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530349"
---
# <a name="namespace-ace-flag-constants"></a>Constantes d’indicateur ACE d’espace de noms

La liste suivante répertorie les valeurs possibles du champ **indicateurs** dans une entrée de Access Control WMI (ACE).

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**l’objet \_ hérite de l' \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Les objets enfants non-conteneurs héritent de l’entrée du contrôle d’accès comme entrée de contrôle d’accès effective.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**\_ACE d’héritage de conteneur \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



L’entrée du contrôle d’accès a un effet sur les espaces de noms enfants, ainsi que sur l’espace de noms actuel.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**AUCUNE \_ propagation d' \_ entrée de contrôle d’accès \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



L’entrée du contrôle d’accès s’applique uniquement à l’espace de noms actuel et aux enfants immédiats.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**HÉRITer \_ uniquement \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



L’entrée du contrôle d’accès s’applique uniquement aux espaces de noms enfants.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**\_ACE hérité**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Cette valeur n’est pas définie par les clients, mais elle est signalée aux clients lorsque la source d’une entrée de contrôle d’accès est un espace de noms parent.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Établissement de l’héritage de la sécurité des espaces de noms](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




