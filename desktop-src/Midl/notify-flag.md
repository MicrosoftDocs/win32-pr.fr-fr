---
title: attribut notify_flag
description: L’attribut \ notification \_ Flag \ fournit une notification indiquant si une routine de serveur est appelée.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag MIDL de l’attribut
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030062"
---
# <a name="notify_flag-attribute"></a>attribut notifier l' \_ indicateur

L’attribut **\[ \_ indicateur \] Notify** fournit une notification indiquant si une routine serveur est appelée.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de la procédure* 
</dt> <dd>

Nom de la procédure distante à laquelle la procédure de l’indicateur de notification \_ est associée.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ \_ indicateur \] Notify** est semblable à l’utilisation de l’attribut **\[ Notify \]** .

Le nom de la procédure d' **\[ \_ indicateur \] Notify** est le nom de la procédure distante suffixée par l' **\_ \_ indicateur Notify**. La procédure de **\_ notification d' \_ indicateur** ne nécessite aucun paramètre et ne retourne pas de résultat. Un prototype de cette procédure est également généré dans le fichier d’en-tête. Par exemple, si le fichier IDL contient les éléments suivants :

``` syntax
MyProcedure([in] short S);
```

Spécifiez ce qui suit dans le ACF pour MIDL afin de générer l’appel de **\_ notification \_ Flag** :

``` syntax
[notify_flag] MyProcedure();
```

Le compilateur MIDL génère le code stub du serveur qui contient l’appel suivant à la procédure **\_ notification \_ Flag** :

``` syntax
MyProcedure_notify_flag();
```

Le fichier d’en-tête contiendra un prototype :

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** a la **valeur true** si la routine de serveur est appelée.

## <a name="examples"></a>Exemples

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**indiquer**](notify.md)
</dt> </dl>

 

 




