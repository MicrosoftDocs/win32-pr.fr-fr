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
ms.openlocfilehash: 178faf3d308f7dd282e31a8f0eabf8708bb8b3fe1a0d52a981e65adddb258ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067149"
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

*function-name* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ peut \]** s’appliquer.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un appel avec l' **\[ \] attribut peut ne** pas contenir de paramètres de sortie et est implicitement un **\[** [](idempotent.md) **\]** appel idempotent.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**diffusion**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




