---
UID: ''
title: MessageProc fonction de rappel
description: Le système appelle cette fonction après qu’un événement d’entrée s’est produit dans une boîte de dialogue, une boîte de message, un menu ou une barre de défilement. | MessageProc fonction de rappel
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
ms.openlocfilehash: 6da307d00c9291ab8c27b97c5012c9887b5c12fcbc541beb5a9b7e8c176ec5a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200781"
---
# <a name="messageproc-function"></a>MessageProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Le système appelle cette fonction après qu’un événement d’entrée s’est produit dans une boîte de dialogue, une boîte de message, un menu ou une barre de défilement, mais avant le traitement du message généré par l’événement d’entrée.
La procédure de hook peut surveiller les messages d’une boîte de dialogue, d’une boîte de message, d’un menu ou d’une barre de défilement créée par une application particulière ou toutes les applications.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**MessageProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="code-in"></a>Code [in]

Type : **int**

Type d’événement d’entrée qui a généré le message.
Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | l’événement d’entrée s’est produit lors de échange dynamique de données l’attente de la fin d’une transaction synchrone par la DDEML Management Library (). pour plus d’informations sur DDEML, consultez [bibliothèque de gestion des échange dynamique de données](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | L’événement d’entrée s’est produit dans une boîte de message ou une boîte de dialogue. |
| **MSGF_MENU** 2 | L’événement d’entrée s’est produit dans un menu. |
| **MSGF_SCROLLBAR** 5 | L’événement d’entrée s’est produit dans une barre de défilement. |

### <a name="wparam"></a>wParam

Type : **wParam**

Ce paramètre n'est pas utilisé.

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure [MSG](/windows/win32/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Retours

Type : **LRESULT**

Si le *code* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.

Si le *code* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est fortement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_MSGFILTER](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.

## <a name="remarks"></a>Remarques

Une application installe la procédure de raccordement en spécifiant le type de hook **WH_MSGFILTER** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Si une application qui utilise DDEML et exécute des transactions synchrones doit traiter des messages avant qu’ils ne soient distribués, elle doit utiliser le hook **WH_MSGFILTER** .

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[FRAGMENT](/windows/win32/api/winuser/ns-winuser-msg)

[Hooks](hooks.md)
