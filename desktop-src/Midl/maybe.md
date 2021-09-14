---
title: attribut peut-être
description: Le mot clé \ Maybe \ indique que l’appel de procédure distante n’a pas besoin d’être exécuté à chaque fois qu’il est appelé et que le client n’attend pas de réponse. Notez que le protocole \ Maybe \ n’assure ni la remise, ni l’achèvement de l’appel.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- MIDL d’attribut peut-être
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093429"
---
# <a name="maybe-attribute"></a>attribut peut-être

Le mot clé **\[ peut \]** indiquer que l’appel de procédure distante n’a pas besoin d’être exécuté à chaque fois qu’il est appelé et que le client n’attend pas de réponse. Notez que le protocole **\[ peut \]** ne pas s’assurer de la remise ni de la fin de l’appel.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie des attributs supplémentaires à appliquer à la fonction. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ peut \]** s’appliquer.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

Un appel avec l' **\[ \] attribut peut ne** pas contenir de paramètres de sortie et est implicitement un **\[** [](idempotent.md) **\]** appel idempotent.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**diffusion**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




