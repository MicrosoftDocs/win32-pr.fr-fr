---
description: Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande annuler la suppression dans le menu fichier.
title: FM_UNDELETE_PROC pointeur de fonction (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842420"
---
# <a name="fm_undelete_proc-function-pointer"></a>\_ \_ Pointeur de fonction proc de suppression de la suppression FM

Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande **annuler la suppression** dans le menu **fichier** .

## <a name="syntax"></a>Syntaxe


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndOwner* 
</dt> <dd>

Type : **HWND**

Handle de fenêtre vers le gestionnaire de fichiers. Une DLL d’annulation de suppression doit utiliser ce handle pour spécifier la fenêtre propriétaire d’une boîte de dialogue ou d’une boîte de message que la DLL peut afficher.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Type : **LPSTR**

Adresse d’une chaîne terminée par le caractère null qui contient le nom du répertoire initial.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **DWORD**

Retourne l’une des valeurs suivantes.



| Code de retour                                                                             | Description                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Une erreur est survenue.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Un fichier a été supprimé. Le gestionnaire de fichiers redessine sa fenêtre.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Aucun fichier n’a été supprimé.<br/>                                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




