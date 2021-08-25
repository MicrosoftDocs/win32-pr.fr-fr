---
description: La \_ structure PARSERINFO de PF définit un analyseur à la fois. Dans la \_ structure PARSERINFO de PF, un analyseur est défini par les informations relatives au protocole détecté par l’analyseur.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Structure de PF_PARSERINFO (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889939"
---
# <a name="pf_parserinfo-structure"></a>PF \_ PARSERINFO, structure

La **structure \_ PARSERINFO de PF** définit un analyseur à la fois. Dans la **structure \_ PARSERINFO de PF** , un analyseur est défini par les informations relatives au protocole détecté par l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**szProtocolName**
</dt> <dd>

Nom du protocole détecté par l’analyseur.

</dd> <dt>

**szComment**
</dt> <dd>

Brève description du protocole.

</dd> <dt>

**szHelpFile**
</dt> <dd>

Nom du fichier d’aide de protocole, le cas échéant.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Pointeur vers une [structure \_ FOLLOWSET de PF](pf-followset.md) qui répertorie les protocoles qui peuvent précéder le protocole décrit par la structure **\_ PARSERINFO de PF** . Moniteur réseau ajoute le protocole de l’analyseur au [*jeu suivant*](f.md) de tous les protocoles de l’ensemble.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Pointeur vers une [structure \_ FOLLOWSET de PF](pf-followset.md) qui répertorie le protocole qui peut suivre le protocole décrit par la structure **\_ PARSERINFO de PF** . Moniteur réseau ajoute les protocoles de l’ensemble à l' [*ensemble suivant*](f.md) du protocole de l’analyseur.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Pointeur vers une [structure \_ HANDOFFSET de PF](pf-handoffset.md) qui transmet le protocole décrit par la structure **\_ PARSERINFO de PF** . Moniteur réseau ajoute le protocole de l’analyseur aux [*jeux de remise*](h.md) de tous les protocoles de l’ensemble.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Pointeur vers une [structure \_ HANDOFFSET de PF](pf-handoffset.md) qui répertorie les protocoles que le protocole d’analyseur transmet. Moniteur réseau ajoute les protocoles de cet ensemble au [*jeu de remise*](h.md) du protocole d’analyseur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La **structure \_ PARSERINFO PF** est utilisée dans la **structure \_ PARSERDLLINFO de PF** pour fournir une description d’un analyseur. Moniteur réseau utilise la description de l’analyseur pour mettre à jour le fichier [*Parser.ini*](p.md) et les fichiers ini des analyseurs qui précèdent et suivent le protocole décrit dans la structure **\_ PARSERINFO de PF** .

Un jeu suivant spécifie les protocoles qui suivent un protocole. Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole. Un jeu de suivi est stocké dans le fichier [*Parser.ini*](p.md) . Lorsque l’analyseur est installé pour la première fois, Moniteur réseau met à jour l’ensemble des protocoles de l’analyseur répertoriés dans **pWhoCanPrecedeMe** et **pWhoCanFollowMe**.

Un jeu de remise spécifie les protocoles qui suivent un protocole. L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole. Un jeu de remise est stocké dans les fichiers INI de chaque analyseur. Lorsque l’analyseur est installé pour la première fois, Moniteur réseau met à jour le jeu de remise des protocoles de l’analyseur qui sont répertoriés dans **pWhoHandsOffToMe** et **pWhoDoIHandOffTo**.



| Pour plus d’informations sur                                               | Consultez                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.        | [Analyseurs](parsers.md)                                                       |
| Les jeux d’éléments suivants contiennent.                                        | [Spécification d’un jeu de suivi](specifying-a-follow-set.md)                       |
| Ce que contiennent les jeux de remise.                                       | [Spécification d’un jeu de remise](specifying-a-handoff-set.md)                     |
| Les points d’entrée inclus dans la DLL de l’analyseur.                | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)                       |
| L’implémentation de **ParserAutoInstallInfo**  comprend un exemple. | [Implémentation de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[\_FOLLOWSET PF](pf-followset.md)
</dt> <dt>

[\_HANDOFFSET PF](pf-handoffset.md)
</dt> <dt>

[\_PARSERDLLINFO PF](pf-parserdllinfo.md)
</dt> </dl>

 

 




