---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration pour lui demander d’effectuer une initialisation globale, en particulier l’allocation de mémoire.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Message CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456369"
---
# <a name="cpl_init-message"></a>Message d’initialisation de CPL \_

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour lui demander d’effectuer une initialisation globale, en particulier l’allocation de mémoire.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’initialisation est réussie, la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doit retourner une valeur différente de zéro. Sinon, elle doit retourner zéro.

Si [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retourne la valeur zéro, l’application de contrôle met fin à la communication et libère la dll contenant l’application du panneau de configuration.

## <a name="remarks"></a>Remarques

Comme il s’agit de la seule façon pour une application du panneau de configuration de signaler une condition d’erreur, l’application doit allouer de la mémoire en réponse à ce message.

Ce message est envoyé immédiatement après le chargement de la DLL contenant l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
