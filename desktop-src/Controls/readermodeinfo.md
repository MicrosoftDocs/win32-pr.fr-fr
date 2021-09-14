---
title: READERMODEINFO, structure
description: Contient les informations requises pour initialiser la fonction DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO, structure Windows, contrôles
- PREADERMODEINFO, pointeur de structure, contrôles Windows
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117149"
---
# <a name="readermodeinfo-structure"></a>READERMODEINFO, structure

\[**READERMODEINFO** est pris en charge par Windows XP avec Service Pack 2 (SP2). Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures.\]

Contient les informations requises pour initialiser la fonction [**DoReaderMode**](doreadermode.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obligatoire. Taille de la structure en octets. Affectez à ce paramètre la valeur **sizeof (READERMODE)** avant d’appeler [**DoReaderMode**](doreadermode.md).

</dd> <dt>

**HWND**
</dt> <dd>

Type : **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obligatoire. Handle de la fenêtre à utiliser pour le mode lecteur.

</dd> <dt>

**fFlags**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indicateurs personnalisant les fonctionnalités de la fenêtre du mode lecteur. Ce paramètre peut avoir la valeur 0 ; Sinon, une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                  | Signification                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | Définit le curseur au centre de la zone spécifiée en **PRC**. Si cet indicateur n’est pas spécifié, la position du curseur reste inchangée.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt> </dl>       | Autorise uniquement le défilement vertical.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt> </dl> | Autorise uniquement le défilement horizontal.<br/>                                                                                                     |



 

</dd> <dt>

**République**
</dt> <dd>

Type : **LPRECT**

</dd> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie la zone de défilement dans la fenêtre du mode lecteur. Si ce membre a la **valeur null**, la fenêtre entière est utilisée comme zone de défilement.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Type : **PFNREADERSCROLL**

</dd> <dd>

Pointeur vers une fonction de rappel [*ReaderScroll*](readerscroll.md) définie par l’application, utilisée pour notifier l’application que la fenêtre doit faire défiler dans une direction particulière.

</dd> <dt>

**fFlags**
</dt> <dd>

Type : **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Pointeur vers une fonction de rappel [*TranslateDispatch*](translatedispatch.md) définie par l’application, utilisée pour obtenir la première notification de tous les messages envoyés à la fenêtre du mode lecteur.

</dd> <dt>

**lParam**
</dt> <dd>

Type : **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Informations supplémentaires requises par l’application, lues par l’appelant dans la fonction de rappel [*ReaderScroll*](readerscroll.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas déclarée dans un en-tête public. Pour l’utiliser, vous devez inclure la déclaration ci-dessus dans votre propre en-tête.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista, Windows les \[ applications de bureau vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>          |



 

