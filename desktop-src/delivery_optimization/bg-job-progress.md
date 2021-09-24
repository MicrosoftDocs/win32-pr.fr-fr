---
title: Structure BG_JOB_PROGRESS (Deliveryoptimization. h)
description: La structure BG_JOB_PROGRESS fournit des informations de progression relatives aux tâches, telles que le nombre d’octets et de fichiers transférés. Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Structure BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f948b9b1150550fad432b0b816f8d435f2af0b4d
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521176"
---
# <a name="bg_job_progress-structure"></a>Structure BG_JOB_PROGRESS

La structure **BG_JOB_PROGRESS** fournit des informations de progression relatives aux tâches, telles que le nombre d’octets et de fichiers transférés. Pour les travaux de chargement, la progression s’applique au fichier de téléchargement, pas au fichier de réponse.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**BytesTotal**
</dt> <dd>

Nombre total d’octets à transférer pour tous les fichiers du travail. Si la valeur est BG_SIZE_UNKNOWN, la taille totale de tous les fichiers du travail n’a pas été déterminée. L’optimisation de la distribution ne définit pas cette valeur si elle ne peut pas déterminer la taille de l’un des fichiers. Par exemple, si le fichier ou le serveur spécifié n’existe pas, l’optimisation de la remise ne peut pas déterminer la taille du fichier.

Si vous téléchargez des plages à partir du fichier, **bytesTotal** comprend le nombre total d’octets que vous souhaitez télécharger à partir du fichier.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Nombre d’octets transférés.

</dd> <dt>

**FilesTotal**
</dt> <dd>

Nombre total de fichiers à transférer pour ce travail.

</dd> <dt>

**FilesTransferred**
</dt> <dd>

Nombre de fichiers transférés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





