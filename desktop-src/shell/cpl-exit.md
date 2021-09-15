---
description: Envoyé une fois à la fonction CPlApplet d’une application du panneau de configuration avant la publication de la DLL contenant l’application du panneau de configuration.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Message CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412580"
---
# <a name="cpl_exit-message"></a>\_Message de sortie cpl

Envoyé une fois à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration avant la publication de la dll contenant l’application du panneau de configuration.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.

## <a name="remarks"></a>Notes

Ce message est envoyé après l’envoi du dernier message d' [**\_ arrêt de cpl**](cpl-stop.md) .

En réponse à ce message, une application du panneau de configuration doit libérer toute la mémoire qu’elle a allouée et effectuer un nettoyage au niveau global.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
