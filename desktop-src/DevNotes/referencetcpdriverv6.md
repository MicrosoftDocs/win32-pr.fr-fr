---
description: Obtient une référence à un objet pilote TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 7c8fc1a24b812608db74fa16b8dafc323fe48442d61d7d7b35c0d371c0828ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571769"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6 fonction)

Obtient une référence à un objet pilote TCP V6.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDriverObject* \[ à\]
</dt> <dd>

Pointeur vers une structure **d' \_ objet de pilote** . Pour plus d’informations, consultez la documentation du kit WDK.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne l' **état \_ Success**. En cas d’échec, il retourne le code d’état approprié.

## <a name="remarks"></a>Remarques

Cette fonction ne peut être appelée qu’à partir du mode noyau. L’appelant doit décrémenter le décompte de références en appelant la fonction **ObDereferenceObject** lorsqu’il a fini d’utiliser l’objet.

Cette fonction est implémentée dans Drvref. lib, qui est disponible au téléchargement. consultez [Windows bibliothèque d’API de référence de pilote réseau](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




