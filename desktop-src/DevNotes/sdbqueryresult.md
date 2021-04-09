---
description: Contient les résultats de l’interrogation de la base de données de shims pour un exécutable correspondant.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: SDBQUERYRESULT, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950530"
---
# <a name="sdbqueryresult-structure"></a>SDBQUERYRESULT, structure

Contient les résultats de l’interrogation de la base de données de shims pour un exécutable correspondant.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**atrExes**
</dt> <dd>

Valeurs **TAGREF** des fichiers exécutables correspondants. Notez que **sdb \_ Max \_ exe** est défini sur 16.

</dd> <dt>

**adwExeFlags**
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)
</dt> </dl> </dd> <dt>

**atrLayers**
</dt> <dd>

Valeurs **TAGREF** des couches correspondantes. Notez que **le \_ nombre maximal de \_ couches sdb** est défini sur 8.

</dd> <dt>

**dwLayerFlags**
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)
</dt> </dl> </dd> <dt>

**trApphelp**
</dt> <dd>

Valeur **TAGREF** du message AppHelp du fichier exécutable correspondant.

</dd> <dt>

**dwExeCount**
</dt> <dd>

Nombre d’éléments dans **atrExes**.

</dd> <dt>

**dwLayerCount**
</dt> <dd>

Nombre d’éléments dans **atrLayers**.

</dd> <dt>

**Guidid ne**
</dt> <dd>

GUID du dernier fichier exécutable.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)
</dt> </dl> </dd> <dt>

**dwCustomSDBMap**
</dt> <dd>

Mappage des bases de données de shims personnalisées. Les bits correspondants sont définis si **rgGuidDB** est valide.

</dd> <dt>

**rgGuidDB**
</dt> <dd>

GUID des bases de données de shims. Notez que **sdb \_ Max \_ SDBS** est défini sur 16.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




