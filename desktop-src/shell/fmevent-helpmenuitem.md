---
description: Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque l’utilisateur appuie sur la touche F1 sur un élément de commande de menu ou de barre d’outils. L’extension doit appeler WinHelp, avec le paramètre HWND de cette fonction défini sur la valeur du paramètre HWND de l’extension.
title: Message FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971918"
---
# <a name="fmevent_helpmenuitem-message"></a>\_Message FMEVENT HELPMENUITEM

Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque l’utilisateur appuie sur la touche F1 sur un élément de commande de menu ou de barre d’outils. L’extension doit appeler [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), avec le paramètre *HWND* de cette fonction défini sur la valeur du paramètre *HWND* de l’extension.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*uItem* 
</dt> <dd>

Valeur qui identifie l’élément de commande de menu ou de barre d’outils pour lequel vous souhaitez obtenir de l’aide. La procédure d’extension utilise cette valeur pour déterminer la meilleure façon d’appeler [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une procédure DLL d’extension doit retourner zéro si elle traite ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_HELPSTRING FMEVENT**](fmevent-helpstring.md)
</dt> </dl>

 

 




