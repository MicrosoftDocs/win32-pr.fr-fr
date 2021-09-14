---
description: Les méta-qualificateurs affinent la définition des méta-constructions dans le modèle CIM en clarifiant l’utilisation réelle d’une déclaration de classe ou de propriété dans la syntaxe MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Qualificateurs méta
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918795"
---
# <a name="meta-qualifiers"></a>Qualificateurs méta

Les méta-qualificateurs affinent la définition des méta-constructions dans le modèle CIM en clarifiant l’utilisation réelle d’une déclaration de classe ou de propriété dans la syntaxe MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe est une classe d’association utilisée pour décrire une relation entre deux autres classes. L’absence de ce qualificateur indique que la classe n’est pas une classe d’association. Ce qualificateur s’exclut mutuellement avec l' **indication**. Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique si la classe d’objets définit une indication. Ce qualificateur s’exclut mutuellement avec l' **Association**. La valeur par défaut est **false**.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Qualificateurs WMI](wmi-qualifiers.md)
</dt> <dt>

[Ajout d’un qualificateur](adding-a-qualifier.md)
</dt> </dl>

 

 




