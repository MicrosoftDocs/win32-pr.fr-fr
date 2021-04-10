---
title: Instruction de classe
description: Définit la classe de la boîte de dialogue.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menus de l’instruction de classe et autres ressources
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940924"
---
# <a name="class-statement"></a>Instruction de classe

Définit la classe de la boîte de dialogue.

L’instruction de **classe** s’affiche dans la section facultative avant l’instruction main de la [**boîte de dialogue**](dialog-resource.md) . Si aucune classe n’est fournie, la classe de boîte de dialogue standard est utilisée.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*type*
</dt> <dd>

Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue. Si la procédure de fenêtre pour la classe ne traite pas un message qui lui est envoyé, elle doit appeler la fonction [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) pour s’assurer que tous les messages sont correctement gérés pour la boîte de dialogue. Une classe privée peut utiliser **DefDlgProc** comme procédure de fenêtre par défaut. La classe doit être inscrite avec le membre **cbWndExtra** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) définie sur **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Notes

L’instruction **Class** ne doit être utilisée qu’avec des cas spéciaux, car elle remplace le traitement normal d’une boîte de dialogue. L’instruction de **classe** convertit une boîte de dialogue en une fenêtre de la classe spécifiée ; en fonction de la classe, cela peut entraîner des résultats indésirables. N’utilisez pas les noms de classe de contrôle redéfinis avec cette instruction.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction de **classe** :

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DIALOGUE**](dialog-resource.md)
</dt> </dl>

 

 