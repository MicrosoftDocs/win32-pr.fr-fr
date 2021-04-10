---
description: Utilisé pour permettre au mode utilisateur de mieux comprendre la zone de découpage pour Windows sur le bureau. Ce découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: NtGdiDdResetVisrgn, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847029"
---
# <a name="ntgdiddresetvisrgn-function"></a>NtGdiDdResetVisrgn fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Utilisé pour permettre au mode utilisateur de mieux comprendre la zone de découpage pour Windows sur le bureau. Ce découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Pointeur vers l’objet en mode utilisateur de toute surface appartenant au périphérique DirectDraw pour lequel le découpage doit être réinitialisé. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Le découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur. Les parties en mode noyau de DirectDraw et de Windows Graphics Device Interface (GDI) maintiennent un compteur qui est incrémenté chaque fois que la liste de découpage de l’ensemble du bureau change. Un appel à cette fonction enregistre ce compteur avec chaque surface principale DirectDraw existante sur le système.

À un moment ultérieur, lorsque l’une de ces surfaces principales est modifiée par une opération [IDirectDrawSurface7 :: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) ou [IDirectDrawSurface7 :: Lock](/previous-versions/ms858221(v=msdn.10)) (voir la documentation du DDK), le compteur enregistré avec la surface est comparé au compteur global. Si ces valeurs sont différentes, un code d’erreur DDERR \_ VISRGNCHANGED est renvoyé au code du mode utilisateur. Le code en mode utilisateur réinterroge ensuite le découpage actuel du bureau, appelle **NtGdiDdResetVisrgn** et réessaye le IDirectDrawSurface7 :: BLT appliqué à la surface principale, en respectant le nouveau découpage. Finalement, le découpage échantillonné par le code en mode utilisateur sera le même que le découpage actuel possédé par le mode noyau, et IDirectDrawSurface7 :: BLT sera autorisé à continuer.

Il est conseillé aux applications d’utiliser l’interface [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) ou [IDirect3DDevice8 ::P](/previous-versions/ms889707(v=msdn.10)) méthode renouvely pour gérer les modifications de découpage asynchrones. Ces constructions implémentent le découpage asynchrone selon une méthode automatisée et indépendante du système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des clients de bas niveau](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
