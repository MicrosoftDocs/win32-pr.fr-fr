---
title: Structure BG_FILE_PROGRESS (Deliveryoptimization. h)
description: La structure BG_FILE_PROGRESS fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Structure BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 03d84fba3ac9747639d0e2992e63e201d7498118
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521011"
---
# <a name="bg_file_progress-structure"></a>Structure BG_FILE_PROGRESS

La structure **BG_FILE_PROGRESS** fournit des informations de progression relatives aux fichiers, telles que le nombre d’octets transférés.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**BytesTotal**
</dt> <dd>

Taille du fichier en octets. Si l’optimisation de la distribution ne peut pas déterminer la taille du fichier (par exemple, si le fichier ou le serveur n’existe pas), la valeur est DO_UNKNOWN_FILE_SIZE.

Si vous téléchargez des plages à partir d’un fichier, **bytesTotal** reflète le nombre total d’octets que vous souhaitez télécharger à partir du fichier.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Nombre d’octets transférés.

</dd> <dt>

**Terminé**
</dt> <dd>

Pour les téléchargements, la valeur est **true** si le fichier est disponible pour l’utilisateur ; dans le cas contraire, la valeur est **false**. Les fichiers sont à la disposition de l’utilisateur après l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) . Si la méthode **Complete** génère une erreur temporaire, les fichiers traités avant l’erreur sont à la disposition de l’utilisateur. les autres ne le sont pas. Utilisez le membre **terminé** pour déterminer si le fichier est disponible pour l’utilisateur une fois l' **opération terminée** .

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour déterminer si l’optimisation de la remise a transféré le fichier, vous pouvez :

-   Comparez **bytesTransferred** à **bytesTotal**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile :: GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





