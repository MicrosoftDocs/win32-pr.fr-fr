---
title: ReaderScroll fonction de rappel
description: Fonction de rappel définie par l’application utilisée lorsque le pointeur de la souris est déplacé dans la partie de la fenêtre en mode lecteur qui a été déclarée comme zone de défilement active.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll, fonction de rappel des contrôles Windows
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117133"
---
# <a name="readerscroll-callback-function"></a>ReaderScroll fonction de rappel

\[*ReaderScroll* peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Fonction de rappel définie par l’application utilisée lorsque le pointeur de la souris est déplacé dans la partie de la fenêtre en mode lecteur qui a été déclarée comme zone de défilement active.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PRMI* \[ dans\]
</dt> <dd>

Type : **PREADERMODEINFO**

Pointeur vers la structure [**READERMODEINFO**](readermodeinfo.md) qui a été passée à la fonction [**DoReaderMode**](doreadermode.md) . Cette structure définit la fenêtre du mode lecteur et la zone de défilement active.

</dd> <dt>

*DX* \[ dans\]
</dt> <dd>

Type : **int**

Distance à faire défiler horizontalement. Si l' \_ indicateur RMF VERTICALONLY est défini dans la structure [**READERMODEINFO**](readermodeinfo.md) , cette valeur est toujours 0.

</dd> <dt>

*dy* \[ dans\]
</dt> <dd>

Type : **int**

Distance à faire défiler verticalement. Si l' \_ indicateur RMF HORIZONTALONLY est défini dans la structure [**READERMODEINFO**](readermodeinfo.md) , cette valeur est toujours 0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Cette fonction doit toujours retourner **true**.

## <a name="remarks"></a>Notes

Lorsque l’application reçoit une notification de cette fonction, l’application est chargée de faire défiler la fenêtre en mode lecteur dans le sens spécifié par les paramètres *DX* et *dy* .

## <a name="examples"></a>Exemples

L’exemple suivant présente une implémentation de cette fonction à l’aide d’une fonction personnalisée pour effectuer le défilement.


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista, Windows les \[ applications de bureau vista uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>          |



 

