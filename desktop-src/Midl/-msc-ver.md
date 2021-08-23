---
title: commutateur/msc_ver
description: Le \_ commutateur/MSC ver est utilisé pour permettre à MIDL de générer du code qui comprend des optimisations pour les différentes versions des compilateurs Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /commutateur msc_ver MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010224e5339ef89e05d1d96630dbedc0cb453eb8dafb4dd5e9c6edb3c24cc00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811369"
---
# <a name="msc_ver-switch"></a>\_commutateur/MSC ver

Le commutateur **/MSC \_ ver** est utilisé pour permettre à MIDL de générer du code qui comprend des optimisations pour les différentes versions des compilateurs Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*Numéro de version \_* 
</dt> <dd>

spécifie un numéro de version entier du compilateur Microsoft Visual C++ qui sera utilisé pour compiler les stubs client et serveur de l’application distribuée. Le numéro de version par défaut est 1100, qui correspond à Visual C++ version 5,0. Le numéro de version 1200 correspond à Visual C++ version 6,0, et ainsi de suite.

</dd> </dl>

## <a name="remarks"></a>Remarques

En particulier, les valeurs de version de 1100 ou plus font que le compilateur MIDL génère du code à l’aide de la directive **\_ \_ declspec (UUID ())** . Il active également les macros qui utilisent les directives **\_ \_ declspec (selectany)** et **\_ \_ declspec (novtable)** .

 

 




