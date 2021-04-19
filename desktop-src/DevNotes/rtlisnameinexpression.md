---
description: Détermine si une chaîne Unicode correspond au modèle spécifié.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516772"
---
# <a name="rtlisnameinexpression-function"></a>RtlIsNameInExpression fonction)

Détermine si une chaîne Unicode correspond au modèle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Expression* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne du modèle. Cette chaîne peut contenir des caractères génériques. Si le paramètre *ignoreCase* a la valeur true, la chaîne ne doit contenir que des caractères majuscules.

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne à comparer au modèle. Cette chaîne ne peut pas contenir de caractères génériques.

</dd> <dt>

*IgnoreCase* \[ dans\]
</dt> <dd>

**True** pour une correspondance qui ne respecte pas la casse, ou **false** pour la correspondance respectant la casse.

</dd> <dt>

*UpcaseTable* \[ dans, facultatif\]
</dt> <dd>

Pointeur facultatif vers une table de caractères en majuscules à utiliser pour la correspondance qui ne respecte pas la casse. Si ce paramètre a la valeur NULL, la table de caractères majuscules du système par défaut est utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la chaîne correspond au modèle. Si la chaîne ne correspond pas au modèle, cette fonction retourne **false**.

## <a name="remarks"></a>Notes

Cette fonction n’a aucun fichier d’en-tête associé. La bibliothèque d’importation associée, ntdll. lib, est disponible dans Microsoft Windows Driver Kit (WDK). Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
