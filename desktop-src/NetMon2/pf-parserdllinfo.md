---
description: La \_ structure PARSERDLLINFO PF définit les analyseurs situés dans la dll de l’analyseur.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Structure de PF_PARSERDLLINFO (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: caaafeb9883ad514366f91f3834354fbd5ac0850400e61594a5307c4533e0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962849"
---
# <a name="pf_parserdllinfo-structure"></a>PF \_ PARSERDLLINFO, structure

La **structure \_ PARSERDLLINFO PF** définit les analyseurs situés dans la dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**nParsers**
</dt> <dd>

Nombre d’analyseurs dans la DLL de l’analyseur.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Tableau de [structures \_ PARSERINFO PF](pf-parserinfo.md) qui décrivent chaque analyseur dans la dll de l’analyseur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La **structure \_ PARSERDLLINFO PF** est retournée par la fonction d’exportation [ParserAutoInstallInfo](parserautoinstallinfo.md) qui est implémentée dans la dll de l’analyseur. La fonction **ParserAutoInstallInfo** identifie le nombre d’analyseurs dans la dll et utilise un tableau de structures [ \_ PARSERINFO PF](pf-parserinfo.md) pour décrire chaque analyseur.

La \_ structure PARSERDLLINFO de PF doit être allouée à l’aide de **HeapAlloc**.



| Pour plus d’informations sur                                               | Consultez                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.        | [Analyseurs](parsers.md)                                                      |
| Les points d’entrée inclus dans la DLL de l’analyseur.               | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)                      |
| L’implémentation de **ParserAutoInstallInfo**  comprend un exemple. | [Implémentation de ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_PARSERINFO PF](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




