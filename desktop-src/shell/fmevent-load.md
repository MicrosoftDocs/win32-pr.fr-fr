---
description: Envoyé à une DLL d’extension lors du chargement de la DLL par le gestionnaire de fichiers.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Message FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860654"
---
# <a name="fmevent_load-message"></a>FMEVENT le \_ message de chargement

Envoyé à une DLL d’extension lors du chargement de la DLL par le gestionnaire de fichiers.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Adresse d’une structure [**de \_ charge FMS**](fms-load.md) qui spécifie la valeur delta de l’élément de menu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une DLL d’extension doit retourner la **valeur true** pour continuer le chargement de la dll. Si la DLL retourne la **valeur false**, le gestionnaire de fichiers appelle la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) et met fin à toute communication avec la dll d’extension.

## <a name="remarks"></a>Remarques

Une application doit remplir les membres **dwSize nul**, **szMenuName** et **HMENU** dans la structure [**de \_ chargement FMS**](fms-load.md) . Elle doit également enregistrer la valeur du membre **wMenuDelta** et l’utiliser pour identifier les éléments de menu lors de la modification du menu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
