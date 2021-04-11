---
description: Avertit une application lorsque l’IME sélectionné a besoin de la chaîne convertie à partir de l’application. L’application reçoit cette commande via le \_ message de \_ demande de l’IME WM avec les paramètres définis comme indiqué ci-dessous.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202760"
---
# <a name="imr_documentfeed-notification-code"></a>\_Code de notification IMR DOCUMENTFEED

Avertit une application lorsque l’IME sélectionné a besoin de la chaîne convertie à partir de l’application. L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres définis comme indiqué ci-dessous.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une mémoire tampon destinée à contenir la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la structure actuelle de la chaîne de reconversion. Si *lParam* a la valeur **null**, l’application retourne la taille requise pour que la mémoire tampon contienne la structure. La commande retourne 0 en cas d’échec.

## <a name="remarks"></a>Notes

L’IME met en cache les chaînes converties pour une meilleure précision de conversion. L’une des limitations de mise en cache de l’IME est qu’elle perd la chaîne convertie dans les circonstances suivantes :

-   La position du signe insertion de l’application est déplacée par une clé, par exemple, une clé de curseur.
-   La position du signe insertion de l’application est déplacée par la souris.
-   Un nouveau document est ouvert.

Avec la commande **IMR \_ DOCUMENTFEED** , l’IME peut actualiser ses chaînes mises en cache à tout moment. L’utilisation de cette commande améliore la précision de la conversion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>IMM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Commandes du gestionnaire de méthode d’entrée](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




