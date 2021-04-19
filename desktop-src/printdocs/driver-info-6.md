---
description: La \_ structure informations sur le pilote \_ 6 contient des informations sur le pilote d’imprimante.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Structure DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529160"
---
# <a name="driver_info_6-structure"></a>\_Structure info \_ 6 du pilote

La **structure \_ informations \_ sur le pilote 6** contient des informations sur le pilote d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a>Membres

<dl> <dt>

**cVersion**
</dt> <dd>

Version du système d’exploitation pour laquelle le pilote a été écrit. La valeur prise en charge est 3.

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows NT x86, Windows IA64 et Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, C : \\ drivers \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, C : \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de configuration du pilote de périphérique (par exemple, C : \\ drivers \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique (par exemple, C : \\ drivers \\ PSCRPTUI. hlp).

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

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie les noms de pilote d’imprimante antérieurs compatibles avec ce pilote. Par exemple, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Date du package de pilotes, telle que codée dans les fichiers de pilote.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Numéro de version du pilote. Cela provient de la structure de version du pilote.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fabricant.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’URL du fabricant.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’ID de matériel pour le pilote d’imprimante.

</dd> <dt>

**pszProvider**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le fournisseur du pilote d’imprimante (par exemple, « Microsoft Windows 2000 »)

</dd> </dl>

## <a name="remarks"></a>Notes

Les chaînes de ces membres sont contenues dans le fichier. inf qui est utilisé pour ajouter le pilote.

Si vous appelez [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md) avec un *niveau* non égal à 6, puis que vous appelez [**GetPrinterDriver**](getprinterdriver.md) ou [**EnumPrinterDrivers**](enumprinterdrivers.md) avec un *niveau* égal à 6, la structure **\_ informations sur le pilote \_ 6** est retournée avec **pszMfgName**, **pszOEMUrl**, **pszHardwareID** et **pszProvider** défini sur **null**, **dwlDriverVersion** défini sur 0 et **ftDriverDate** défini sur (0,0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le pilote 6W** (Unicode) et **\_ \_ informations sur \_ le pilote** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




