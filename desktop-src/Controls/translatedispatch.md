---
title: TranslateDispatch fonction de rappel
description: Utilisé par le client de la fonction DoReaderMode pour intercepter et gérer explicitement tous les messages Windows ciblés pour la zone de défilement de la fenêtre du mode lecteur. Il s’agit d’une fonction de rappel définie par l’application.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- TranslateDispatch, fonction de rappel des contrôles Windows
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060529"
---
# <a name="translatedispatch-callback-function"></a>TranslateDispatch fonction de rappel

\[*TranslateDispatch* peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Utilisé par le client de la fonction [**DoReaderMode**](doreadermode.md) pour intercepter et gérer explicitement tous les messages Windows ciblés pour la zone de défilement de la fenêtre du mode lecteur. Il s’agit d’une fonction de rappel définie par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpmsg* \[ dans\]
</dt> <dd>

Type : **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message intercepté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si le message a été géré par cette fonction. Sinon, **false**. Si la **valeur est false**, le message est géré par l’implémentation du mode lecteur par défaut. Cette implémentation gère le déplacement et les boutons de la souris, ainsi que les pressions sur les touches.

## <a name="examples"></a>Exemples

L’exemple suivant présente une implémentation de cette fonction.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista, Windows les \[ applications de bureau vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>          |



 

