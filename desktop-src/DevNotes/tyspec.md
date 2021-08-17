---
description: Définit des méthodes de mappage à un ID de classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Énumération TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075753"
---
# <a name="tyspec-enumeration"></a>Énumération TYSPEC

Définit des méthodes de mappage à un ID de classe.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**\_CLSID TYSPEC**
</dt> <dd>

CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**
</dt> <dd>

Extension de nom de fichier. Cette valeur n’est pas prise en charge actuellement.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MimeType**
</dt> <dd>

Type MIME. Cette valeur n’est pas prise en charge actuellement.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nom de fichier TYSPEC**
</dt> <dd>

Nom d'un fichier. Cette valeur n’est pas prise en charge actuellement.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_ProgID TYSPEC**
</dt> <dd>

PROGID. Cette valeur n’est pas prise en charge actuellement.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**
</dt> <dd>

Nom du package. Cette valeur n’est pas prise en charge actuellement.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID TYSPEC**
</dt> <dd>

Un ID d’objet. Cette valeur n’est pas prise en charge actuellement.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’Union **uCLSSPEC** est définie comme suit :

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>Wtypes. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Coinstallation**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
