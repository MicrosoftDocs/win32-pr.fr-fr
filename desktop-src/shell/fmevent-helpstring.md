---
description: Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque le gestionnaire de fichiers souhaite une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.
title: Message FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841280"
---
# <a name="fmevent_helpstring-message"></a>\_Message FMEVENT HELPSTRING

Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque le gestionnaire de fichiers souhaite une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Adresse d’une structure [**\_ HELPSTRING de FMS**](fms-helpstring.md) qui communique les données de chaîne d’aide de l’élément de commande. La **structure \_ HELPSTRING de FMS** identifie l’élément de commande pour lequel une chaîne d’aide est souhaitée, ainsi qu’un handle vers son menu. Une application écrit ensuite la chaîne d’aide appropriée dans le membre **szHelp** de la structure **\_ HELPSTRING de FMS** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




