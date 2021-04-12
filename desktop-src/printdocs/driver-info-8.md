---
description: Contient des informations sur le pilote d’imprimante.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Structure DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320613"
---
# <a name="driver_info_8-structure"></a>\_Structure info \_ 8 du pilote

Contient des informations sur le pilote d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
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

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64.

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

Numéro de version du pilote. Cela provient de la structure de la version du pilote.

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

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le fournisseur du pilote d’imprimante (par exemple, « Microsoft Windows 2000 »).

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le processeur d’impression (par exemple, « WinPrint »).

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie la DLL d’installation du pilote du fournisseur et le point d’entrée.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie les profils de couleur associés au pilote.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le chemin d’accès au fichier. inf du pilote dans le magasin de pilotes. (Consultez la section Notes.) La valeur doit être **null** si les informations sur le pilote \_ \_ 8 sont passées à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Indicateurs d’attribut pour les pilotes d’imprimante. La valeur doit être 0 si les informations sur le pilote \_ \_ 8 sont transmises à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md). Dans le cas contraire, il peut s’agir de n’importe quelle combinaison des indicateurs suivants :



| Nom/valeur de l’indicateur                                                         | Signification                                                                                                                                                                                                                                                                                                                                             | Système d’exploitation minimal                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| prise \_ en \_ charge des packages de pilotes d’imprimante \_<br/> 0x00000001<br/>        | Le pilote d’imprimante fait partie d’un package de pilotes.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| pilote d’imprimante \_ \_ XPS<br/> 0x00000002<br/>                   | Le pilote d’imprimante prend en charge le format Microsoft XPS décrit dans la [spécification XML Paper Specification](/previous-versions/windows/hardware/design/dn641615(v=vs.85))(en anglais), ainsi que dans le [comportement du produit, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| \_bac à \_ sable (sandbox) du pilote d’imprimante \_ activé<br/> 0x00000004<br/>      | Le pilote d’imprimante est compatible avec l' [isolement du pilote d’imprimante](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Pour plus d’informations, consultez [comportement du produit, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| \_classe de pilote d’imprimante \_<br/> 0x00000008<br/>                 | Le pilote d’imprimante est un [pilote d’imprimante de classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| pilote d’imprimante \_ \_ dérivé<br/> 0x00000010<br/>               | Le pilote d’imprimante est un [pilote d’imprimante dérivé](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| le \_ pilote d’imprimante \_ ne \_ partage pas<br/> 0x00000020<br/>        | Les imprimantes qui utilisent ce pilote d’imprimante ne peuvent pas être partagées.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ télécopie catégorie du pilote d’imprimante \_<br/> 0x00000040<br/>         | Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de télécopie](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| \_fichier de \_ catégorie du pilote d’imprimante \_<br/> 0x00000080<br/>        | Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de fichiers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| catégorie de pilote d’imprimante \_ \_ \_ virtuelle<br/> 0x00000100<br/>     | Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes virtuelles](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_service de \_ catégorie de pilote d’imprimante \_<br/> 0x00000200<br/>     | Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de service](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_réinitialisation logicielle du pilote d’imprimante \_ \_ \_ requise<br/> 0x00000400<br/> | Les imprimantes qui utilisent ce pilote d’imprimante doivent suivre les instructions fournies dans la définition de la classe de périphérique USB. Pour plus d’informations, consultez [comportement du produit, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Pointeur vers une chaîne multiple se terminant par un caractère null qui spécifie tous les pilotes d’imprimante principaux dont dépend le pilote. La valeur doit être **null** si les informations sur le **pilote \_ \_ 8** sont passées à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

La première date autorisée des pilotes fournis avec Windows et dont ce pilote dépend.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

La première version autorisée des pilotes fournis avec Windows et dont dépend ce pilote.

</dd> </dl>

## <a name="remarks"></a>Notes

Les chaînes de ces membres sont contenues dans le fichier. inf qui est utilisé pour ajouter le pilote.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le pilote 8W** (Unicode) et **\_ \_ informations sur le pilote \_ 8A** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

