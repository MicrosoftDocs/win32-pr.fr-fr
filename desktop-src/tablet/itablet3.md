---
description: L’interface ITablet3 active l’interrogation multipoint pour l’entrée.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interface ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449842"
---
# <a name="itablet3-interface"></a>Interface ITablet3

L’interface ITablet3 active l’interrogation multipoint pour l’entrée.

## <a name="members"></a>Membres

L’interface **ITablet3** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet3** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITablet3** possède ces méthodes.



| Méthode                                                  | Description                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Récupère le nombre maximal d’entrées prises en charge.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Indique si l’interaction tactile est activée pour cet objet.<br/> |



 

## <a name="remarks"></a>Remarques

Les développeurs ne doivent pas utiliser cette interface

Le code suivant décrit comment l’interface **ITablet3** est définie.

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

