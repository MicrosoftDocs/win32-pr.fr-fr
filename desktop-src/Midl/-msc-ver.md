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
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841429"
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

Spécifie un numéro de version entier du compilateur Microsoft Visual C++ qui sera utilisé pour compiler les stubs client et serveur de l’application distribuée. Le numéro de version par défaut est 1100, qui correspond à Visual C++ version 5,0. Le numéro de version 1200 correspond à Visual C++ version 6,0, et ainsi de suite.

</dd> </dl>

## <a name="remarks"></a>Notes

En particulier, les valeurs de version de 1100 ou plus font que le compilateur MIDL génère du code à l’aide de la directive **\_ \_ declspec (UUID ())** . Il active également les macros qui utilisent les directives **\_ \_ declspec (selectany)** et **\_ \_ declspec (novtable)** .

 

 




