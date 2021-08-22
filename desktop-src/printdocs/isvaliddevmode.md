---
description: La fonction IsValidDevmode vérifie que le contenu d’une structure DEVMODE est valide.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: IsValidDevmode, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100527"
---
# <a name="isvaliddevmode-function"></a>IsValidDevmode fonction)

La fonction **IsValidDevmode** vérifie que le contenu d’une structure DEVMODE est valide.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevmode* \[ dans\]
</dt> <dd>

Pointeur vers le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) à valider.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Taille en octets de la mémoire tampon d’octets en entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True** si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) est structurellement valide. Si des erreurs mineures sont détectées, la fonction les corrige et retourne la **valeur true**.

**False**, si le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) présente un ou plusieurs problèmes structurels significatifs. Par exemple, son membre **dmSize** est mal aligné ou spécifie une mémoire tampon qui est trop petite. **False** également si **PDevmode** a la **valeur null**.

## <a name="remarks"></a>Remarques

Aucun champ de pilote d’imprimante privée de l' [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) n’est activé, mais uniquement les champs publics.

Les appelants doivent utiliser **dmSize** + **dmDriverExtra** pour **DevmodeSize** uniquement s’ils peuvent garantir que la taille de la mémoire tampon d’entrée est au moins égale à celle du grand. Étant donné que la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) est généralement des données non fiables, les valeurs qui se trouvent dans la mémoire tampon d’entrée au niveau des offsets **dmSize** et **dmDriverExtra** sont également non fiables.

Cette fonction est exécutable dans Least-Privileged contexte de compte d’utilisateur (LUA).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Winspool. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **IsValidDevmodeW** (Unicode) et **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




