---
description: Définit la structure du fichier d’en-tête Moniteur réseau.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Structure de CAPTUREFILE_HEADER_VALUES (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367415"
---
# <a name="capturefile_header_values-structure"></a>\_Structure de valeurs d’en-tête CAPTUREFILE \_

La structure des **\_ \_ valeurs d’en-tête CAPTUREFILE** définit la structure du fichier d’en-tête Moniteur réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Membres

<dl> <dt>

**Signature**
</dt> <dd>

Identificateur unique : 'GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binaire, codé décimal (mineur). La valeur de ce membre doit être égale à zéro (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Décimale codée binaire (majeure). Cette valeur doit être 2.

</dd> <dt>

**MacType**
</dt> <dd>

Type de topologie.

</dd> <dt>

**Confirmé**
</dt> <dd>

Heure de la capture.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Table d’index de frames.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Taille de la table d’index de frames.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Décalage des données utilisateur.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Longueur des données de l’utilisateur.

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

Décalage des données de commentaire.

</dd> <dt>

**CommentDataLength**
</dt> <dd>

Longueur des données de commentaire.

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

Décalage de la structure des **statistiques** .

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Longueur de la structure des **statistiques** .

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Décalage de la structure **NETWORKINFO** .

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Longueur de la structure **NETWORKINFO** .

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

Ce membre n’est pas utilisé.

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

Ce membre n’est pas utilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




