---
description: Contient des informations sur les données AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Structure APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: e9aab48760af45772cf77b4f943144ceab4104ebfd762c8ec7402caf1de8cfec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103759"
---
# <a name="apphelp_data-structure"></a>\_Structure de données APPHELP

Contient des informations sur les données AppHelp.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwFlags**
</dt> <dd>

Ce paramètre peut prendre l’une des valeurs suivantes.

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

**dwSeverity**
</dt> <dd>

Ce paramètre peut être APPTYPE \_ None (0).

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

Identificateur d’aide HTML.

</dd> <dt>

**szAppName**
</dt> <dd>

Nom de l’application.

</dd> <dt>

**trExe**
</dt> <dd>

[**TAGREF**](tagref.md) du fichier exécutable correspondant.

</dd> <dt>

**szURL**
</dt> <dd>

URL du lien AppHelp online.

</dd> <dt>

**szLink**
</dt> <dd>

Texte de lien pour **szURL**.

</dd> <dt>

**szAppTitle**
</dt> <dd>

Titre du message AppHelp.

</dd> <dt>

**szContact**
</dt> <dd>

Informations de contact du fournisseur.

</dd> <dt>

**szDetails**
</dt> <dd>

Message AppHelp détaillé.

</dd> <dt>

**dwData**
</dt> <dd>

Données définies par l’utilisateur et gérées par l’application.

</dd> <dt>

**bSPEntry**
</dt> <dd>

Ce membre a la **valeur true** si cette entrée figure dans la base de données Service Pack et la **valeur false** dans le cas contraire.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




