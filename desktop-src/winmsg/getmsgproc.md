---
UID: ''
title: GetMsgProc fonction de rappel
description: Le système appelle cette fonction lorsqu’une fonction de message reçoit un message à partir d’une file d’attente de messages d’application.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e5c51f2abe8b3660ae40bae05c13428e0622fd4d5c4b8020fea8caa924a35681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200791"
---
# <a name="getmsgproc-function"></a>GetMsgProc fonction)

## <a name="-description"></a>-Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) . Le système appelle cette fonction chaque fois que la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) a récupéré un message à partir d’une file d’attente de messages d’application.
Avant de retourner le message récupéré à l’appelant, le système transmet le message à la procédure de Hook.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**GetMsgProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-paramètres

### <a name="code-in"></a>Code [in]

Type : **int**

Spécifie si la procédure de raccordement doit traiter le message.
Si le *code* est **HC_ACTION**, la procédure de raccordement doit traiter le message.
Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Spécifie si le message a été supprimé de la file d’attente.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | Le message n’a pas été supprimé de la file d’attente. (Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .) |
| **PM_REMOVE** 0x0001 | Le message a été supprimé de la file d’attente. (Une application appelée **GetMessage** ou appelée fonction  **PeekMessage** , en spécifiant l’indicateur **PM_REMOVE** .)|

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure [MSG](/windows/desktop/api/winuser/ns-winuser-msg) qui contient des détails sur le message.

## <a name="-returns"></a>-retourne

Si le *code* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).

Si le *code* est supérieur ou égal à zéro, il est fortement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_GETMESSAGE](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de hook n’appelle pas **CallNextHookEx**, la valeur de retour doit être égale à zéro.

## <a name="-remarks"></a>-Remarques

La procédure de hook **GetMsgProc** peut examiner ou modifier le message.
Une fois que la procédure de Hook a retourné le contrôle au système, la fonction **GetMessage** ou **PeekMessage** retourne le message, ainsi que toutes les modifications, à l’application qui l’a appelée à l’origine.

Une application installe cette procédure de hook en spécifiant le type de hook **WH_GETMESSAGE** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[FRAGMENT](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)
