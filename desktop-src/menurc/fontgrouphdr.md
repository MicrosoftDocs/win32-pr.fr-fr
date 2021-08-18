---
title: FONTGROUPHDR, structure
description: Contient les informations nécessaires à une application pour accéder à une police spécifique. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menus de la structure FONTGROUPHDR et autres ressources
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51b307b7f5798a57e344096fe46227edf97babbf3547c4c851d71fd8ecdc28da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734477"
---
# <a name="fontgrouphdr-structure"></a>FONTGROUPHDR, structure

Contient les informations nécessaires à une application pour accéder à une police spécifique. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Membres

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre de polices individuelles associées à cette ressource.

</dd> <dt>

**DE**
</dt> <dd>

Type : **[ **dilocataire**](direntry.md)**

</dd> <dd>

Structure qui contient un identificateur ordinal unique pour chaque police de la ressource. Le **membre est** un espace réservé pour le tableau de longueur variable de structures de [**diloyer**](direntry.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **FONTGROUPHDR** suit les données pour les polices individuelles dans le. Fichier res. Le compilateur de ressources ajoute automatiquement la structure **FONTGROUPHDR** , généralement comme dernière entrée dans le fichier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Dilocataire**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

 





