---
description: La \_ structure informations sur le pilote \_ 2 identifie un pilote d’imprimante, le numéro de version du pilote, l’environnement pour lequel le pilote a été écrit, le nom du fichier dans lequel le pilote est stocké, et ainsi de suite.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Structure DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517690"
---
# <a name="driver_info_2-structure"></a>\_Structure informations sur le pilote \_ 2

La **structure \_ informations \_ sur le pilote 2** identifie un pilote d’imprimante, le numéro de version du pilote, l’environnement pour lequel le pilote a été écrit, le nom du fichier dans lequel le pilote est stocké, et ainsi de suite.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**cVersion**
</dt> <dd>

Version du système d’exploitation pour laquelle le pilote a été écrit. La valeur prise en charge est 3.

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, « QMS 810 »).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, « c : \\ drivers \\pscript.dll »).

</dd> <dt>

**pDataFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, « c : \\ drivers \\ Qms810. PPD »).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la configuration. dll du pilote de l’appareil (par exemple, « c : \\ drivers \\Pscrptui.dll »).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le pilote 2S** (Unicode) et **\_ \_ informations sur le pilote \_ 2A** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




