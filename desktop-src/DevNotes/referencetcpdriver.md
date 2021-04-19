---
description: Obtient une référence à un objet pilote TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539251"
---
# <a name="referencetcpdriver-function"></a>ReferenceTcpDriver fonction)

Obtient une référence à un objet pilote TCP v4.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
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

## <a name="remarks"></a>Notes

Cette fonction ne peut être appelée qu’à partir du mode noyau. L’appelant doit décrémenter le décompte de références en appelant la fonction **ObDereferenceObject** lorsqu’il a fini d’utiliser l’objet.

Cette fonction est implémentée dans Drvref. lib, qui est disponible au téléchargement. Consultez [bibliothèque d’API de référence du pilote réseau Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




