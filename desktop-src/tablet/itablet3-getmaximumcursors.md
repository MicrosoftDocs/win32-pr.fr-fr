---
description: La méthode GetMaximumCursors récupère le nombre maximal de curseurs pris en charge par un périphérique tablette.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3 :: GetMaximumCursors, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533949"
---
# <a name="itablet3getmaximumcursors-method"></a>ITablet3 :: GetMaximumCursors, méthode

La méthode **GetMaximumCursors** récupère le nombre maximal de curseurs pris en charge par un périphérique tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMaximumCursors* 
</dt> <dd>

Nombre maximal d’entrées que l’appareil prend en charge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite ; sinon, retourne un code d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




