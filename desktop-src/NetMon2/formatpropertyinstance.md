---
description: Met en forme les données d’instance de propriété à l’aide du formateur générique fourni par Moniteur réseau.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: FormatPropertyInstance, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021107"
---
# <a name="formatpropertyinstance-function"></a>FormatPropertyInstance fonction)

La fonction **FormatPropertyInstance** met en forme les données d’instance de propriété à l’aide du formateur générique fourni par Moniteur réseau.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpPropertyInst* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [PROPERTYINST](propertyinst.md) qui contient les données d’instance.

En entrée, le formateur générique prend les données d’instance de l’un des membres de l’Union **PROPERTYINST** et convertit ces données en chaîne mise en forme prédéfinie.

Lors de la sortie, le formateur générique définit le membre **szPropertyText** de la structure **PROPERTYINST** sur un pointeur vers la chaîne mise en forme.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur de NMerr. h.

## <a name="remarks"></a>Notes

La DLL de l’analyseur appelle indirectement la fonction **FormatPropertyInstance** lorsque le formateur générique est requis pour mettre en forme les données à afficher dans le volet d’informations de l’interface utilisateur Moniteur réseau. Pour appeler **FormatPropertyInstance** , spécifiez-le dans le membre **InstanceData** de la structure [PROPERTYINFO](propertyinfo.md) lorsque vous définissez la propriété.

> [!Note]  
> L’analyseur ne reconnaît pas la fonction qui est appelée lorsqu’il doit mettre en forme une instance d’une propriété. La fonction peut être **FormatPropertyInstance** ou une fonction de format personnalisée définie par l’analyseur. L’analyseur appelle la fonction de format spécifiée par le membre **InstanceData** de la structure **PROPERTYINFO** pour la propriété.

 

Pour plus d’informations et pour obtenir un exemple d’implémentation de [formatproperties](formatproperties.md), consultez [implémentation de formatproperties](implementing-formatproperties.md). Pour plus d’informations sur la façon dont le formateur générique met en forme les différents types de données, consultez [sortie du formateur générique](generic-formatter-output.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




