---
description: La \_ structure informations sur le pilote \_ 3 contient des informations sur le pilote d’imprimante.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Structure DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530593"
---
# <a name="driver_info_3-structure"></a>\_Structure info du pilote \_ 3

La **structure \_ informations \_ sur le pilote 3** contient des informations sur le pilote d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DRIVER_INFO_3 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a>Membres

<dl> <dt>

**cVersion**
</dt> <dd>

Version du système d’exploitation pour laquelle le pilote a été écrit. Les valeurs prises en charge sont 3 et 4, qui représentent respectivement les pilotes v3 et v4.

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, « QMS 810 »).

</dd> <dt>

**pEnvironment**
</dt> <dd>

pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, « C : \\ drivers \\Pscript.dll »).

</dd> <dt>

**pDataFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, « C : \\ drivers \\ Qms810. PPD »).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de la configuration du pilote de périphérique (par exemple, « C : \\ drivers \\Pscrptui.dll »).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique.

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Pointeur vers une mémoire tampon MultiSZ qui contient une séquence de chaînes terminées par le caractère null. Chaque chaîne se terminant par un caractère NULL dans la mémoire tampon contient le nom d’un fichier dont le pilote dépend. La séquence de chaînes se termine par une chaîne vide de longueur nulle. Si **pDependentFiles** n’a pas la **valeur null** et qu’il ne contient aucun nom de fichier, il pointe vers une mémoire tampon qui contient deux chaînes vides.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie une analyse de langage (par exemple, « PJL Monitor »). Ce membre peut être **null** et doit être spécifié uniquement pour les imprimantes capables d’effectuer une communication bidirectionnelle.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut du travail d’impression (par exemple, « EMF »).

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le pilote 3W** (Unicode) et **\_ \_ informations sur le pilote \_ 3A** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




