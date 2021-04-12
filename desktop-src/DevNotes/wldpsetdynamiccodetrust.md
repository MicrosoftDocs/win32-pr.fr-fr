---
description: Définit une liste de révocation de code dynamique de la liste de révocation de certificats .NET sur disque pour .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: WldpSetDynamicCodeTrust, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393023"
---
# <a name="wldpsetdynamiccodetrust-function"></a>WldpSetDynamicCodeTrust fonction)

Définit une liste de révocation de code dynamique de la liste de révocation de certificats .NET sur disque pour .NET.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileHandle* 
</dt> <dd>

Handle vers un fichier de code dynamique sur disque.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1803 \[ uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




