---
description: Le mode d’affichage a changé.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541667"
---
# <a name="ec_display_changed"></a>\_affichage EC \_ modifié

Le mode d’affichage a changé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers un tableau d’interfaces [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) pour les broches d’entrée du convertisseur vidéo. Si *lParam2* est égal à zéro, ce paramètre peut avoir la **valeur null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *lParam2* est égal à zéro, *lParam1* contient un seul pointeur **IPIN** ou est égal à **null**. Si *lParam2* est supérieur à zéro, *lParam1* contient un tableau de pointeurs **IPIN** et le nombre d’éléments dans le tableau est donné par *lParam2*.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Le gestionnaire de graphique de filtre arrête temporairement le graphique, puis se déconnecte et reconnecte le convertisseur vidéo. Elle ne passe pas l’événement à l’application.

## <a name="remarks"></a>Notes

Les convertisseurs vidéo peuvent envoyer cet événement en réponse à un message [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) . Le message **WM \_ DISPLAYCHANGE** indique que l’utilisateur a modifié la résolution d’affichage.

Pendant la connexion de code confidentiel, la plupart des convertisseurs vidéo sélectionnent un format basé sur le mode d’affichage actuel. Si le mode d’affichage change, le convertisseur vidéo devra peut-être choisir un autre format. En envoyant ce message, le convertisseur signale au gestionnaire de graphique de filtre qu’il doit être reconnecté. Pendant la reconnexion, le convertisseur peut sélectionner un nouveau format. Si la reconnexion échoue, le gestionnaire de graphique de filtre envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) à l’application.

### <a name="enhanced-video-renderer"></a>Convertisseur vidéo amélioré

Un présentateur personnalisé pour le [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) doit envoyer cet événement à EVR si l’appareil Direct3D du présentateur change. Définissez *lParam1* et *lParam2* sur zéro ; EVR ignore les paramètres d’événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

