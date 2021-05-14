---
description: Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers. Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.
title: Structure FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842160"
---
# <a name="fms_toolbarload-structure"></a>\_TOOLBARLOAD-structure FMS

Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers. Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, de la structure. Le gestionnaire de fichiers définit la taille avant d’appeler l’extension et vérifie la taille après le retour de la procédure d’extension.

</dd> <dt>

**lpButtons**
</dt> <dd>

Type : **LPEXT \_ Button**

</dd> <dd>

Adresse d’un tableau de structures [**de \_ bouton ext**](ext-button.md) .

</dd> <dt>

**cButtons**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre de structures [**de \_ bouton ext**](ext-button.md) dans le tableau vers lequel pointe le membre **lpButtons** . Ce nombre est égal au nombre de boutons et de séparateurs à ajouter à la barre d’outils.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre de boutons représentés par la bitmap donnée.

</dd> <dt>

**idBitmap**
</dt> <dd>

Type : **Word**

</dd> <dd>

Identificateur d’une ressource bitmap dans le fichier exécutable de la DLL d’extension. La ressource bitmap contient des images pour le nombre de boutons spécifiés par **cBitmaps**. Le gestionnaire de fichiers charge la ressource bitmap, puis l’utilise pour afficher les boutons.

</dd> <dt>

**hBitmap**
</dt> <dd>

Type : **HBITMAP**

</dd> <dd>

Handle d’une image bitmap que le gestionnaire de fichiers utilisera pour obtenir et afficher des images de bouton si **idBitmap** est égal à 0.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




