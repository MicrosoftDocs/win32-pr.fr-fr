---
description: Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU). Utilisé par CreateMRUListW.
title: MRUINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991117"
---
# <a name="mruinfo-structure"></a>MRUINFO, structure

Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU). Utilisé par [**CreateMRUListW**](createmrulist.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille de la structure.

</dd> <dt>

**uMax**
</dt> <dd>

Type : **uint**

</dd> <dd>

Nombre maximal d’entrées dans la liste des fichiers récents.

</dd> <dt>

**fFlags**
</dt> <dd>

Type : **uint**

</dd> <dd>

Un ou plusieurs des indicateurs suivants.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINAIRE** (0x0001)


</dt> <dd>

Les données sont stockées dans le Registre sous forme de données binaires plutôt que de données de chaîne.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Écrire les modifications apportées à la version des fichiers MRU stockés dans le registre uniquement lors de l’ajout d’un nouvel élément ou lorsque les ressources de la liste MRU sont libérées de la mémoire. Notez que la version active des fichiers MRU en mémoire est mise à jour immédiatement en réponse à toute modification de contenu ou de commande.

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

Type : **HKEY**

</dd> <dd>

Handle vers la clé actuellement ouverte, ou l’une des valeurs prédéfinies suivantes sous lesquelles stocker les données MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ Current \_ User**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ local \_ machine**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Type : **LPCTSTR**

</dd> <dd>

Sous-clé dans laquelle stocker les données MRU.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Type : **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Pointeur vers une fonction de comparaison de données facultative qui peut être utilisée pour déterminer si un élément est présent dans la liste MRU. Cela est utile lorsque la liste MRU a été créée avec l’indicateur **\_ binaire MRU** . Si ce membre a la **valeur null**, les fonctions de comparaison de chaînes standard sont utilisées ; pour les données binaires, une comparaison de mémoire directe est utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas définie dans un fichier d’en-tête. Vous devez le définir vous-même.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |
| Noms Unicode et ANSI<br/>   | **MRUINFOW** (Unicode) et **MRUINFOA** (ANSI)<br/>  |



 

 




