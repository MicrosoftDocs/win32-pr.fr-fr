---
description: Structure utilisée par la fonction SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Structure PPROTECT_FILE_ENTRY (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404369"
---
# <a name="pprotect_file_entry-structure"></a>Structure d’entrée de \_ fichier PPROTECT \_

\[Cette structure peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de cette structure a été supprimée dans Windows Vista et Windows Server 2008. Utilisez à la place les fonctions prises en charge listées dans [fonctions WRP](wfp-functions.md) .\]

Structure utilisée par la fonction [**SfcGetFiles**](sfcgetfiles.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**SourceFileName**
</dt> <dd>

Pointeur vers une valeur de chaîne contenant le nom de fichier du fichier source. La valeur est **null** si le fichier n’a pas été renommé lors de l’installation.

</dd> <dt>

**FileName**
</dt> <dd>

Pointeur vers la valeur de chaîne contenant le nom de fichier de destination plus le chemin d’accès complet au fichier.

</dd> <dt>

**InfName**
</dt> <dd>

Pointeur vers la valeur de chaîne contenant le nom du fichier INF qui fournit les informations de mise en page. Ce paramètre peut avoir la **valeur null** lors de l’utilisation de la disposition par défaut.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                 |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




