---
title: Structure _VIDEOINFOHEADER
description: La \_ structure VIDEOINFOHEADER contient des informations sur un flux vidéo et inclut une \_ structure BITMAPINFOHEADER qui définit le format d’un frame individuel.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Structure de _VIDEOINFOHEADER Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586799"
---
# <a name="_videoinfoheader-structure"></a>\_VIDEOINFOHEADER, structure

La structure **\_ VIDEOINFOHEADER** contient des informations sur un flux vidéo et inclut une structure **\_ BITMAPINFOHEADER** qui définit le format d’un frame individuel.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**rcSource**
</dt> <dd>

La structure **Rect** qui spécifie la fenêtre vidéo source.

</dd> <dt>

**rcTarget**
</dt> <dd>

Structure **Rect** qui spécifie la fenêtre vidéo de destination.

</dd> <dt>

**dwBitRate**
</dt> <dd>

Valeur **DWORD** qui spécifie le débit de données approximatif du flux vidéo, en bits par seconde.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

Valeur **DWORD** qui spécifie le taux d’erreur des données du flux vidéo, en erreurs de bits par seconde.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**Référence \_** Valeur de temps qui spécifie la durée d’affichage moyenne de la image vidéo, en unités de 100 nanosecondes.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Structure **\_ BITMAPINFOHEADER** Win32 qui contient des informations de couleur et de dimension pour la bitmap de l’image vidéo.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





