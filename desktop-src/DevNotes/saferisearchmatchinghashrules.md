---
description: Obtient le niveau d’une règle d’identification de hachage qui correspond au hachage spécifié.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483648"
---
# <a name="saferisearchmatchinghashrules-function"></a>SaferiSearchMatchingHashRules fonction)

Obtient le niveau d’une règle d’identification de hachage qui correspond au hachage spécifié.

Cette fonction n’a pas de bibliothèque d’importation associée et n’est pas déclarée dans un en-tête public. Vous devez définir un pointeur de fonction avec la signature de cette fonction, et vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Advapi32.dll.

Nous vous recommandons d’utiliser la fonction [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) pour évaluer les stratégies de restriction logicielle.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HashAlgorithm* \[ dans, facultatif\]
</dt> <dd>

Identificateur de l’algorithme utilisé pour créer le hachage.

</dd> <dt>

*pHashBytes* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient le hachage.

</dd> <dt>

*dwHashSize* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau *pHashBytes* .

</dd> <dt>

*dwOriginalImageSize* \[ dans, facultatif\]
</dt> <dd>

Taille, en octets, de l’image d’origine à partir de laquelle le hachage a été calculé.

</dd> <dt>

*pdwFoundLevel* \[ à\]
</dt> <dd>

Pointeur vers l’identificateur de niveau pour la règle d’identification de hachage correspondante.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Réservé. Définissez cette valeur sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True** si la fonction réussit ; Sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
