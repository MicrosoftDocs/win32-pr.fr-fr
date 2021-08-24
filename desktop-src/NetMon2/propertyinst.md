---
description: La structure PROPERTYINST définit une instance d’une propriété dans une partie des données reconnues. Moniteur réseau alloue et remplit une structure PROPERTYINST lorsqu’une propriété est attachée à la capture.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: PROPERTYINST, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0d1c338fb8b4e63f03bff422e25578132476f70d932e8f17d5b0c39a0f6416e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778499"
---
# <a name="propertyinst-structure"></a>PROPERTYINST, structure

La structure **PROPERTYINST** définit une instance d’une propriété dans une partie des données reconnues. Moniteur réseau alloue et remplit une structure **PROPERTYINST** lorsqu’une propriété est attachée à la capture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Membres

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

Pointeur vers la structure [PROPERTYINFO](propertyinfo.md) qui définit la propriété.

</dd> <dt>

**szPropertyText**
</dt> <dd>

Pointeur vers une chaîne qui est affichée dans le volet d’informations de l’interface utilisateur Moniteur réseau.

</dd> <dt>

**lpData**
</dt> <dd>

Pointeur vers le début des données de la propriété. L’analyseur détermine l’emplacement où les données de la propriété démarrent.

</dd> <dt>

**lpByte**
</dt> <dd>

Pointeur vers les données d' **octets** .

</dd> <dt>

**lpWord**
</dt> <dd>

Pointeur vers les données du **mot** .

</dd> <dt>

**lpDword**
</dt> <dd>

Pointeur vers les données **DWORD** .

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Pointeur vers les données [**LARGEINT**](largeint.md) .

</dd> <dt>

**lpSysTime**
</dt> <dd>

Pointeur vers les données [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Pointeur vers une structure [PROPERTYINSTEX](propertyinstex.md) . Le membre **lpPropertyInstEx** est utilisé uniquement lorsque vous appelez [AttachPropertyInstanceEx](attachpropertyinstanceex.md).

Si **lpPropertyInstEx** est utilisé, vous devez définir le membre **DATALENGTH** sur 0xFFFF.

</dd> <dt>

**DataLength**
</dt> <dd>

Longueur des données de cette instance de la propriété. Si le membre **lpPropertyInstEx** pointe vers une structure [**PROPERTYINSTEX**](propertyinstex.md) , vous devez affecter à **DATALENGTH** la valeur 0xFFFF.

</dd> <dt>

**Niveau**
</dt> <dd>

Informations de niveau.

</dd> <dt>

**HelpID**
</dt> <dd>

Identificateur du contexte du fichier d’aide.

</dd> <dt>

**IFlags**
</dt> <dd>

Indicateur de condition d’erreur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **PROPERTYINST** définit une instance d’une propriété jointe. L’analyseur accède à la structure **PROPERTYINST** par le biais de plusieurs fonctions d’assistance. Par exemple, lorsque la fonction [**FormatPropertyInstance**](formatpropertyinstance.md) est appelée pour mettre en forme les données d’une propriété, elle modifie le membre **szPropertyText** de la structure **PROPERTYINST** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

