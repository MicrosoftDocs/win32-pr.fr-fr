---
description: La structure de la SESSION contient des informations sur la session active.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Structure de SESSION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747669"
---
# <a name="session-structure"></a>Structure de SESSION

\[Cette structure contient des informations requises uniquement lorsque vous utilisez les fonctions **DeleteExtractedFiles** et **extract** , qui ne sont pas prises en charge. Cette documentation est fournie à titre d’information uniquement.\]

La structure de la **session** contient des informations sur la session active.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a>Membres

<dl> <dt>

**agir**
</dt> <dd>

l’action à effectuer. Ce membre peut être l’une des valeurs du type énuméré suivant.

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

**hflist**
</dt> <dd>

Handle d’une liste de fichiers spécifiée sur la ligne de commande. Ce type de données est déclaré comme suit :

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

Indicateur qui signale si plusieurs fichiers CAB doivent être traités. Si cette valeur est **true**, les armoires de continuation sont traitées.

</dd> <dt>

**fOverwrite**
</dt> <dd>

Indicateur qui signale si les fichiers existants doivent être remplacés. Si cette valeur est **true**, les fichiers existants sont remplacés.

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

Indicateur qui signale si le dernier `printf` appel a les caractères de saut de ligne ( `\n` ). Si cette valeur est **true**, le dernier `printf` appel n’a pas inclus les caractères de saut de ligne.

</dd> <dt>

**fSelfExtract**
</dt> <dd>

Indicateur qui indique si un fichier cab est auto-extractible. Si cette valeur est **true**, l’armoire est auto-extractible.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Longueur de la partie exécutable (. exe) d’un fichier cab à extraction automatique.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Longueur de la partie du fichier CAB d’un fichier cab à extraction automatique.

</dd> <dt>

**ahfSelf**
</dt> <dd>

Descripteurs de fichiers dans le fichier CAB.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

Nombre d’erreurs rencontrées pendant la session d’extraction.

</dd> <dt>

**hfdi**
</dt> <dd>

Handle vers le contexte FDI. Ce type de données est déclaré comme suit :

`typedef void FAR *HFDI; `

</dd> <dt>

**ERF**
</dt> <dd>

Structure d’erreur FDI. Consultez [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**cFiles**
</dt> <dd>

Nombre de fichiers traités.

</dd> <dt>

**cbTotalBytes**
</dt> <dd>

Nombre total d’octets extraits.

</dd> <dt>

**perr**
</dt> <dd>

L’étape FDI.

</dd> <dt>

**ateliers**
</dt> <dd>

Erreur du fichier de débordement. Ce membre peut être l’une des valeurs du type énuméré suivant.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbSpill**
</dt> <dd>

Taille du fichier de débordement demandé.

</dd> <dt>

**achSelf**
</dt> <dd>

Nom du fichier exécutable (. exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

Mémoire tampon de mise en forme du message.

`#define cbMAX_LINE          256`

</dd> <dt>

**achLine**
</dt> <dd>

Mémoire tampon de mise en forme de ligne.

</dd> <dt>

**achLocation**
</dt> <dd>

Répertoire de sortie.

</dd> <dt>

**achFile**
</dt> <dd>

Nom de fichier actuel en cours d’extraction.

</dd> <dt>

**achDest**
</dt> <dd>

Nom du fichier de destination forcé.

</dd> <dt>

**achCabPath**
</dt> <dd>

Chemin d’accès à examiner pour un fichier CAB.

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

Indicateur qui signale si le fichier CAB actuel est le premier traité. Si la valeur est **true**, le premier fichier CAB n’est pas traité.

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

Indicateur qui spécifie si les informations de réserve doivent être fournies. Si la valeur est **true**, les informations sont rendues disponibles.

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

Ce membre fournit un moyen de déterminer les entrées **ACAB** à utiliser si nous traitons tous les fichiers d’un jeu de fichiers CAB (**fAllCabinet** a la valeur **true**).

</dd> <dt>

**acab**
</dt> <dd>

Les deux dernières entrées dans le jeu de fichiers CAB. Cette structure est définie comme suit :

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

**achZap**
</dt> <dd>

Préfixe à supprimer du nom de fichier.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

Fichier CAB actuel.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

Argc à extraction automatique par défaut.

</dd> <dt>

**pArgv**
</dt> <dd>

Pointeur vers un pointeur vers le argv à extraction automatique par défaut \[ \] .

</dd> <dt>

**fDestructive**
</dt> <dd>

Indicateur qui réduit l’espace disque nécessaire lorsque la propriété a la valeur **true**.

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

Si **fDestructive** a la valeur **true**, extraire uniquement le dossier actif.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Extraction**](extract.md)
</dt> </dl>

 

 
