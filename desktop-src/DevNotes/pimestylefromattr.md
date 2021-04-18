---
description: Récupère les styles pour un attribut donné.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: PIMEStyleFromAttr fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540180"
---
# <a name="pimestylefromattr-function"></a>PIMEStyleFromAttr fonction)

Récupère les styles pour un attribut donné.

## <a name="syntax"></a>Syntaxe


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attr* \[ dans\]
</dt> <dd>

Ce paramètre peut prendre les valeurs suivantes.

<dl> <dt>

<span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_ FIXEDCONVERTED** (5)
</dt> <dt>

<span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_ ENTRÉE** (0)
</dt> <dt>

<span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_ \_Erreur d’entrée** (4)
</dt> <dt>

<span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_ MAX** (5)
</dt> <dt>

<span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_ MIN** (0)
</dt> <dt>

<span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_ CIBLE \_ convertie** (1)
</dt> <dt>

<span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_ \_NOTCONVERTED cible** (4)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une structure **IMESTYLE** représentant les paramètres de couleur et de non-couleur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

La structure **IMESTYLE** est définie comme suit :

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



 

 
