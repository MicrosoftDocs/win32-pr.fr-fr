---
description: Champ de type dans une entrée de contrôle d’accès (ACE) qui détermine si l’ACE est une entrée du contrôle d’accès qui autorise ou refuse l’accès.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Constantes de type d’ACE d’espace de noms (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540032"
---
# <a name="namespace-ace-type-constants"></a>Constantes de type d’ACE d’espace de noms

Champ de **type** dans une entrée de contrôle d’accès (ACE) qui détermine si l’ACE est une entrée du contrôle d’accès qui autorise ou refuse l’accès.

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Activer**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



L’ACE autorise l’accès à l’espace de noms.


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Interdire**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



L’ACE refuse l’accès à l’espace de noms.


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

 

 




