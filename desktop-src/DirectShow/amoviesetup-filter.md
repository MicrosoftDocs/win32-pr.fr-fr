---
description: La \_ structure de filtre AMOVIESETUP contient des informations sur l’inscription d’un filtre.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Structure AMOVIESETUP_FILTER (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535339"
---
# <a name="amoviesetup_filter-structure"></a>\_Structure de filtre AMOVIESETUP

La structure de **\_ filtre AMOVIESETUP** contient des informations sur l’inscription d’un filtre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Identificateur**
</dt> <dd>

Identificateur de classe du filtre.

</dd> <dt>

**strName**
</dt> <dd>

Nom du filtre.

</dd> <dt>

**dwMerit**
</dt> <dd>

Mérite de filtre. Utilisé par l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) lors de la construction d’un graphique de filtre. Pour obtenir la liste des valeurs mérites, consultez [mérite](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Nombre d’éléments dans le tableau *lpPin* . Si *lpPin* a la **valeur null**, affectez la valeur zéro à ce membre.

</dd> <dt>

**lpPin**
</dt> <dd>

Pointeur vers un tableau de structures [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) , de taille *nPins*. Chaque membre de ce tableau décrit un code confidentiel sur le filtre.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur l’utilisation de cette structure, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md). Utilisez cette structure uniquement pour les filtres qui sont enregistrés dans la catégorie de filtre par défaut (CLSID \_ LegacyAmFilterCategory). Pour inscrire un filtre dans une autre catégorie, utilisez la méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , comme décrit dans [implémentation de DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> Le fichier d’en-tête ComBase. h est fourni avec les [classes de base DirectShow](directshow-base-classes.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>ComBase. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DirectShow](directshow-structures.md)
</dt> </dl>

 

 




